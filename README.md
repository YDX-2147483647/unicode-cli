# Unicode CLI

A small command-line utility to look up Unicode characters. It is capable of both forward and reverse search.

## Inspect a Unicode string

Show flags, code point, block name, and character name of each character in a string.

```shell
$ unicode-cli inspect "Uü’(ꝰ)"
aa-c-u-     55 Basic Latin LATIN CAPITAL LETTER U
ua-c--l     FC Latin-1 Supplement LATIN SMALL LETTER U WITH DIAERESIS
u---i--   2019 General Punctuation RIGHT SINGLE QUOTATION MARK
a-b----     28 Basic Latin LEFT PARENTHESIS
ua-ci-l   A770 Latin Extended-D MODIFIER LETTER US
a-b----     29 Basic Latin RIGHT PARENTHESIS
```

<details>
<summary>Meaning of the flags</summary>

1. `a`/`u`: **A**SCII or **U**nicode.
2. `a`/`-`: **a**lphabetic or not.
3. `b`/`-`: mirrored in **b**idirectional context or not.
4. `c`/`-`: **c**ased or not.
5. `i`/`-`: case **i**gnorable or not.
6. `u`/`-`: **u**ppercase or not.
7. `l`/`-`: **l**owercase or not.

</details>

## List all code points

List all characters in a block.

```shell
$ unicode-cli ls Emoticons
Emoticons
😀😁😂😃😄😅😆😇😈😉😊😋😌😍😎😏😐😑😒😓😔😕😖😗😘😙😚😛😜😝😞😟😠😡😢😣😤😥😦😧😨😩😪😫😬😭😮😯😰😱😲😳😴😵😶😷😸😹😺😻😼😽😾😿🙀🙁🙂🙃🙄🙅🙆🙇🙈🙉🙊🙋🙌🙍🙎🙏

$ unicode-cli ls 'Mahjong Tiles'
Mahjong Tiles
🀀🀁🀂🀃🀄🀅🀆🀇🀈🀉🀊🀋🀌🀍🀎🀏🀐🀑🀒🀓🀔🀕🀖🀗🀘🀙🀚🀛🀜🀝🀞🀟🀠🀡🀢🀣🀤🀥🀦🀧🀨🀩🀪🀫🀬🀭🀮🀯
```

## Create a Unicode string

Compose characters by themselves, names, or code points.

```shell
$ unicode-cli compose u 'COMBINING DIAERESIS' 77FF
ü矿
```
