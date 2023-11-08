---
layout: center
class: scale-110
---

```yml{all|7,11-13,15-17,19-21}
name: CI
                                          
on:
  pull_request:

jobs:
  changes:
    ...
  check-formatting:
    ...
  lint:
    needs: changes
    if: ${{ needs.changes.outputs.lint == 'true' }}
    ...
  build:
    needs: changes
    if: ${{ needs.changes.outputs.src == 'true' }}
    ...
  test:
    needs: changes
    if: ${{ needs.changes.outputs.test == 'true' }}
    ...
```