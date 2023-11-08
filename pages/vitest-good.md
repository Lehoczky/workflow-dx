---
layout: center
class: scale-110
---

```ts
import { expect, test } from "vitest"

test("we can add numbers together", () => {
  expect(1 + 1).toBe(2)
})
```

<v-click>

```shell
> vitest run


 DEV  v0.34.6 C:/Users/zole02/Projects/gh-actions-dx

 ✓ tests/sum.test.ts (1)
   ✓ we can add numbers together

 Test Files  1 passed (1)
      Tests  1 passed (1)
   Start at  17:57:08
   Duration  748ms (transform 112ms, setup 0ms, collect 97ms, tests 3ms, environment 0ms, prepare 131ms)
```

</v-click>

<!-- 
Test can fail as well ->

 -->