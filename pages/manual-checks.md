---
layout: center
class: scale-140
---

<span style="margin-left: 14px;">package.json:</span>

```json
{
    "scripts": {
        "dev": "vite",
        "build": "tsc && vite build",
        "test": "vitest run",
        "format:check": "prettier . --check --ignore-unknown",
        "eslint:check": "eslint . --ext .js,.ts --max-warnings=0"
  }
}
```

<v-click>

```shell
npm install
npm run format:check
npm run eslint:check
npm run test
npm run build
```

</v-click>

<!-- 

Let's see how to implement a workflow that does just this for us ->
 -->