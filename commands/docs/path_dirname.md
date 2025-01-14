---
title: path dirname
categories: |
  path
version: 0.84.0
path: |
  Get the parent directory of a path.
usage: |
  Get the parent directory of a path.
---

# <code>{{ $frontmatter.title }}</code> for path

<div class='command-title'>{{ $frontmatter.path }}</div>

## Signature

```> path dirname --replace --num-levels```

## Parameters

 -  `--replace {string}`: Return original path with dirname replaced by this string
 -  `--num-levels {int}`: Number of directories to walk up


## Input/output types:

| input        | output       |
| ------------ | ------------ |
| list\<string\> | list\<string\> |
| string       | string       |
## Examples

Get dirname of a path
```shell
> '/home/joe/code/test.txt' | path dirname
/home/joe/code
```

Get dirname of a list of paths
```shell
> [ /home/joe/test.txt, /home/doe/test.txt ] | path dirname
╭───┬───────────╮
│ 0 │ /home/joe │
│ 1 │ /home/doe │
╰───┴───────────╯

```

Walk up two levels
```shell
> '/home/joe/code/test.txt' | path dirname -n 2
/home/joe
```

Replace the part that would be returned with a custom path
```shell
> '/home/joe/code/test.txt' | path dirname -n 2 -r /home/viking
/home/viking/code/test.txt
```
