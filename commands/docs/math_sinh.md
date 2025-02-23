---
title: math sinh
categories: |
  math
version: 0.84.0
math: |
  Returns the hyperbolic sine of the number.
usage: |
  Returns the hyperbolic sine of the number.
---

# <code>{{ $frontmatter.title }}</code> for math

<div class='command-title'>{{ $frontmatter.math }}</div>

## Signature

```> math sinh ```


## Input/output types:

| input        | output       |
| ------------ | ------------ |
| list\<number\> | list\<number\> |
| number       | number       |
## Examples

Apply the hyperbolic sine to 1
```shell
> 1 | math sinh
1.1752011936438014
```


**Tips:** Command `math sinh` was not included in the official binaries by default, you have to build it with `--features=extra` flag