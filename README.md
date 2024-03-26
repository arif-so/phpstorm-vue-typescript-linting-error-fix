## Fix "Vue: Cannot find module '...' or its corresponding type declaration" error

I fixed my issue by making a file called 'vue-shim.d.ts' in the src folder and then restarting PHPStorm.

vue-shim.d.ts code:
```javascript
declare module "*.vue" {
  import { defineComponent } from "vue";
  const component: ReturnType<typeof defineComponent>;
  export default component;
}
```
Source:  https://github.com/vuejs/vue-cli/issues/1198

## Preview
![Project preview image](/preview.png) 
