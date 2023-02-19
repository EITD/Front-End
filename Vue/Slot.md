# Slot

Use `slot` when define template.

```html

  <template id="cpn">
    <div>
      <div>
        {{message}}
      </div>
      
      <slot><button>button</button></slot>
    </div>
  </template>
```

Use `slot`, replace slot value.

```html
<cpn></cpn>
<cpn><span style="color:red;">222</span></cpn>
```

# Named Scoped slot

> Custom slot **order**. Otherwise slots are ordered according to the order of code.
> 

```html

  <div id="app">
    <cpn>
      <span>no</span>
      <span slot="left">left</span>
      
      <template v-slot:center>mid</template>
      
      <template #right>right</template>
    </cpn>
  </div>

  
  <template id="cpn">
    <div>
      <slot name="left">left</slot>
      <slot name="center">mid</slot>
      <slot name="right">right</slot>
      <slot>no</slot>
    </div>
  </template>
```