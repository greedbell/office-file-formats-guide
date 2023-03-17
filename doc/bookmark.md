# Bookmark

- [3.3 Example of a Bookmark](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-doc/b5e6b16c-4c09-4eda-81bb-9757385dc9ba)

书签需要的数据有 `SttbfBkmk` `Plcfbkf` `Plcfbkl`，通过 `FibRgFcLcb97` 可以查到各个数据在 `Table Stream` 中的位置和长度。

## SttbfBkmk

按顺序记录各种书签的名称

## Plcfbkf

记录书签开始位置和 [FBKF](#fbkf)

### FBKF

书签信息

- ibkl
- bkc: 指向 [BKC](#bkc)

### BKC

The BKC structure contains information about how a bookmark interacts with tables

记录书签在 table 中的位置

- `itcFirst`: 指向对应 Plcfbkl
- `fPub`
- `itcLim`
- `fNative`
- `fColC`

## Plcfbkl

记录书签结束位置

- `aCP`: CP 数组

最后一个 CP 记录？？，其它 CP 记录对应书签的？？

## References

- [Text-Extract-Word-0.04](https://metacpan.org/dist/Text-Extract-Word/source/lib/Text/Extract/Word.pm#L124)
  https://github.com/kertom/BrowserFSTest/blob/4efdac4d5d7894cee6cc025baa1e5ffefc1fe988/src/app/home/word.js#L61
