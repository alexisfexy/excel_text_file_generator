# Excel To Text File Generation

Transforms excel sheet with desired text file names & content into text files. Optional parameter to include text transformation too.


## Overview of Requirements:
1. excel file with columns for text file names & columns for file contents
2. mapping of column indexes & any alterations you want to the text (e.g remove prefix, capitalize, etc). See below for example.

```
{<Column Description>: {"file_name": (<index>, <callable of text alterations>),
                           "content": (<index>,, <callable of text alterations>}}

EXAMPLE: 
{
    "split":
        {"file_name": (2, lambda string: string.removeprefix("    SplitKey.").removesuffix(": ")),
           "content": (4, None)}
}```
