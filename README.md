## I solved my problem by creating a file named vue-shim.d.ts in the src directory and then restarting
Source:  https://github.com/vuejs/vue-cli/issues/1198

```javascript
declare module "*.vue" {
  import { defineComponent } from "vue";
  const component: ReturnType<typeof defineComponent>;
  export default component;
}
```

## Project preview
![Project preview image](/preview.png) 
