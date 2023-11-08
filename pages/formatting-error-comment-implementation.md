---
layout: center
class: scale-140
---

```yml{all|2|4-11|12-18|all}
- name: Check formatting 🎨
  id: formatting
  run: npm run format:check
  
- name: Report formatting failure
  if: always() && steps.formatting.outcome == 'failure'
  uses: marocchino/sticky-pull-request-comment@v2
  with:
    header: formatting-message-header
    message: |
      Formatting errors found! ❌
  
- name: Remove last formatting failure message
  if: always() && steps.formatting.outcome != 'failure'
  uses: marocchino/sticky-pull-request-comment@v2
  with:
    header: formatting-message-header
    delete: true
```
