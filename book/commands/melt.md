---
title: melt
version: 0.69.1
dataframe: |
  Unpivot a DataFrame from wide to long format
usage: |
  Unpivot a DataFrame from wide to long format
---

# <code>{{ $frontmatter.title }}</code> for dataframe

<div class='command-title'>{{ $frontmatter.dataframe }}</div>

## Signature

```> melt --columns --values --variable-name --value-name```

## Parameters

 -  `--columns {table}`: column names for melting
 -  `--values {table}`: column names used as value columns
 -  `--variable-name {string}`: optional name for variable column
 -  `--value-name {string}`: optional name for value column

## Examples

melt dataframe
```shell
> [[a b c d]; [x 1 4 a] [y 2 5 b] [z 3 6 c]] | into df | melt -c [b c] -v [a d]
```