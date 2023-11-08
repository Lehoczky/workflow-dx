---
class: text-center
---

```yml{all} {maxHeight:'400px'}
changes:
  runs-on: ubuntu-latest
  outputs:
    lint: ${{ steps.filter.outputs.lint }}
    src: ${{ steps.filter.outputs.src }}
    test: ${{ steps.filter.outputs.test }}
  steps:
    - name: Check out Git repository ⏬
      uses: actions/checkout@v3

    - name: Get changed file categories
      uses: dorny/paths-filter@v2
      id: filter
      with:
        filters: |
          lint:
            - "**/*.{js,ts}"
            - "**/tsconfig*.json"
            - ".eslint*"
            - "package*.json"
          src:
            - "src/**/*.{js,ts}"
            - "**/tsconfig*.json"
            - "package*.json"
          test:
            - "src/**/*.{js,ts}"
            - "tests/**/*.{js,ts}"
            - "**/tsconfig*.json"
            - "package*.json"
```
