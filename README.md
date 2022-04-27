# vue-tsc v-for type error reproduction repo

The related issue is https://github.com/johnsoncodehk/volar/issues/591.

Execute 

```
npm install
npm run typecheck
```

and then you get the following error message

```
src/test.vue:5:29 - error TS2345: Argument of type 'number | keyof Data[]' is not assignable to parameter of type 'number'.
  Type 'string' is not assignable to type 'number'.

5         <div>{{ formatIndex(index) }}</div>
                              ~~~~~
```