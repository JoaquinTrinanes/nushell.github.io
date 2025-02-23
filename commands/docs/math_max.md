---
title: math max
categories: |
  math
version: 0.84.0
math: |
  Returns the maximum of a list of values, or of columns in a table.
usage: |
  Returns the maximum of a list of values, or of columns in a table.
---

# <code>{{ $frontmatter.title }}</code> for math

<div class='command-title'>{{ $frontmatter.math }}</div>

## Signature

```> math max ```


## Input/output types:

| input     | output |
| --------- | ------ |
| list\<any\> | any    |
| table     | record |
## Examples

Find the maximum of list of numbers
```shell
> [-50 100 25] | math max
100
```

Find the maxima of the columns of a table
```shell
> [{a: 1 b: 3} {a: 2 b: -1}] | math max
╭───┬───╮
│ a │ 2 │
│ b │ 3 │
╰───┴───╯
```
