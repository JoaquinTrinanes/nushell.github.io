---
title: dfr first
categories: |
  dataframe
version: 0.84.0
dataframe: |
  Show only the first number of rows or create a first expression
usage: |
  Show only the first number of rows or create a first expression
---

# <code>{{ $frontmatter.title }}</code> for dataframe

<div class='command-title'>{{ $frontmatter.dataframe }}</div>

## Signature

```> dfr first (rows)```

## Parameters

 -  `rows`: starting from the front, the number of rows to return


## Input/output types:

| input | output |
| ----- | ------ |
| any   | any    |

## Examples

Return the first row of a dataframe
```shell
> [[a b]; [1 2] [3 4]] | dfr into-df | dfr first
╭───┬───┬───╮
│ # │ a │ b │
├───┼───┼───┤
│ 0 │ 1 │ 2 │
╰───┴───┴───╯

```

Return the first two rows of a dataframe
```shell
> [[a b]; [1 2] [3 4]] | dfr into-df | dfr first 2
╭───┬───┬───╮
│ # │ a │ b │
├───┼───┼───┤
│ 0 │ 1 │ 2 │
│ 1 │ 3 │ 4 │
╰───┴───┴───╯

```

Creates a first expression from a column
```shell
> dfr col a | dfr first

```


**Tips:** Dataframe commands were not shipped in the official binaries by default, you have to build it with `--features=dataframe` flag