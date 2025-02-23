---
title: path basename
categories: |
  path
version: 0.84.0
path: |
  Get the final component of a path.
usage: |
  Get the final component of a path.
---

# <code>{{ $frontmatter.title }}</code> for path

<div class='command-title'>{{ $frontmatter.path }}</div>

## Signature

```> path basename --replace```

## Parameters

 -  `--replace {string}`: Return original path with basename replaced by this string


## Input/output types:

| input        | output       |
| ------------ | ------------ |
| list\<string\> | list\<string\> |
| string       | string       |
## Examples

Get basename of a path
```shell
> '/home/joe/test.txt' | path basename
test.txt
```

Get basename of a list of paths
```shell
> [ /home/joe, /home/doe ] | path basename
╭───┬─────╮
│ 0 │ joe │
│ 1 │ doe │
╰───┴─────╯

```

Replace basename of a path
```shell
> '/home/joe/test.txt' | path basename -r 'spam.png'
/home/joe/spam.png
```
