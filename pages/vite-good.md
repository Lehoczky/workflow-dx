```text
project/
├── src/
│   ├── main.ts
│   ├── utils.ts
└── index.html
```

<v-click>

```shell
> tsc && vite build

vite v4.5.0 building for production...
✓ 4 modules transformed.
dist/index.html                0.39 kB │ gzip: 0.27 kB
dist/assets/index-368327e1.js  0.88 kB │ gzip: 0.50 kB
✓ built in 176ms
```

</v-click>

<v-click>

```text
project/
├── dist/
|   ├── assets/
|   |     └── index-368327e1.js  
|   └── index.html
```

</v-click>

<!-- 
Builds can also fail though ->


 -->