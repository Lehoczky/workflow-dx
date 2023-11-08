---
class: scale-100 grid grid-items-center
---

```ts
import { expect, test } from "vitest"

test("we can add numbers together", () => {
  expect(1 + 2).toBe(2)
})
```

<v-click>

```shell
> vitest run


 ❯ tests/sum.test.ts (1)
   × we can add numbers together

...

 ❯ tests/sum.test.ts:4:17
      2| 
      3| test("we can add numbers together", () => {
      4|   expect(1 + 2).toBe(2)
       |                 ^
      5| })
      6|

```

</v-click>