---
class: p-1
---
<div class="grid grid-cols-2" style="--slidev-code-margin: 0 6px; transform: scale(0.85) translateY(-52px)">

```yml
check-formatting:
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
```

```yml
lint:
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

    - name: Check lint errors 🧹
      run: npm run eslint:check
```

```yml
build:
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

    - name: Build the app 🏗
      run: npm run build
```

```yml
test:
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

    - name: Run the tests 🧪
      run: npm run test
```

</div>