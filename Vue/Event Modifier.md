# Event Modifier

```jsx
<div id="app">
    
    <div @click="divClick">
        <button @click.stop="btnClick">button1</button>
    </div>
    
    <form action="www.baidu.com">
      <button type="submit" @click.prevent="submitClick">submit</button>
    </form>
    
    <input type="text" @click.enter="keyup">

  </div>
```