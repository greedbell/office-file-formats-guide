# Comment

## [2.3.4 Comments](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-doc/486f5a89-fba5-412f-8ac6-1c551654ddcd)

### [PlcfandTxt](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-doc/ac1c69d1-b6b9-4d2c-8cc6-4300e0ee5921)

### [PlcfandRef](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-doc/9d82ca25-ff21-488c-bee2-dd654935c65a)

#### ATRDPre10

- xstUsrInitl: 评论创建者姓名
- ibst: 评论者姓名 index
- lTagBkmk: bookmark identifier

### [AtrdExtra](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-doc/1b6a50f8-de0c-4020-bce0-06e24660c928)

#### ATRDPost10

- dttm: 评论时间
- b_f_ink_atn: 是否被赞
- c_depth: 评论树结构
- diatrd_parent: 评论树结构

### [SttbfAtnBkmk](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-doc/22d288b9-4d91-4dc6-a2e4-0bb847a1b6a1)

#### ATNBE

评论书签

- bmc: bookmark class?
- lTag: bookmark identifier

## [2.6.1 Character Properties](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-doc/7022285b-9621-42e9-ad4d-4e02c115ef18)

### sprmCFSpec

`U+0005 - An annotation reference character. See PlcfandRef.`

`sprmCFSpec` 值为 `true` 时，文本内容是 `U+0005` 表示是 `commentRangeEnd`

## [2.5.6 FibRgFcLcb97](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-doc/0c9df81f-98d0-454e-ad84-b612cd05b1a4)

### fcPlcfAtnBkf lcbPlcfAtnBkf 对应的 Plcfbkf

- acp: `commentRangeStart` 的 CP
- a_fbkf
  - ibkl: 对应的 `commentRangeEnd` 在 `Plcfbkl` 中的索引

### fcPlcfAtnBkl lcbPlcfAtnBkl 对应的 Plcfbkl

- a_cp: `commentRangeEnd` 的 CP
