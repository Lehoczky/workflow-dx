---
layout: center
class: scale-140
---

```ts
const numbers = [1, 2, 3]
const doubledNumbers = numbers.map(function(number) {
    return number * 2
})
```

<v-click>

```shell
> eslint . --ext .js,.ts --max-warnings=0


C:\Users\zole02\Projects\gh-actions-dx\src\feature.ts
  3:36  warning  Unexpected function expression  prefer-arrow-callback

✖ 1 problem (0 errors, 1 warning)
  0 errors and 1 warning potentially fixable with the `--fix` option.
```

</v-click>

<!--  

- Retro Richard in you team
- likes to use JavaScript syntax from the early 2010's


Fortunately you can set up a linter to throw an error here, because arrow functions have been part of the language for almost a decade now.
 -->