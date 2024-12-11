# vue-default-export

1. Create a `<script setup lang="ts">` Setup.vue component
2. Define the props via an `interface`

```ts
interface Props {
    msg: string;
}

defineProp<Props>();
```

3. Create a `<script lang="ts">` Define component that uses Setup.vue
4. `npm run type-check`


```bash
npm i
npm run type-check
```

You'll see

```ts
src/components/Define.vue:20:1 - error TS4082: Default export of the module has or is using private name 'Props'.

 20 export default defineComponent({
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 21   components: {
    ~~~~~~~~~~~~~~~
... 
 23   },
    ~~~~
 24 });
    ~~~

Found 1 error.
```
