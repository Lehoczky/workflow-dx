<span style="margin-left: 14px;">.github/workflows/ci.yml:</span>

```yml{0|1|3-5|6-9|10-12|13-16|17-19|20-22|23-25|26-28|29-31} {maxHeight:'400px'}
name: CI

on:
  pull_request:

jobs:
  ci:
    runs-on: ubuntu-latest
    steps:
      - name: Check out Git repository ⏬
        uses: actions/checkout@v3

      - name: Set up Node.js 💿
        uses: actions/setup-node@v3
        with:
          node-version: 20

      - name: Install dependencies 📦
        run: npm ci

      - name: Check formatting 🎨
        run: npm run format:check

      - name: Check lint errors 🧹
        run: npm run eslint:check

      - name: Build the app 🏗
        run: npm run build

      - name: Run the tests 🧪
        run: npm run test
```
