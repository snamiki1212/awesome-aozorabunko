# Regex

青空文庫のファイルからルビなどを削除するときの正規表現。

## Plain Text

完全な PlainText にするための正規表現。

> 《》：ルビ
> （例）私《わたくし》は

`《[^》]+》`

> ｜：ルビの付く文字列の始まりを特定する記号
> （例）先生一人｜麦藁帽《むぎわらぼう》を

`｜`

> ［＃］：入力者注　主に外字の説明や、傍点の位置の指定
> 　　　（数字は、JIS X 0213 の面区点番号、または底本のページと行数）
> （例）※［＃「てへん＋劣」、第 3 水準 1-84-77］

`［＃.+?］`

> 上のメタデータ

`---[\s\S\n]*---`

> 下のメタデータ

`^.*：[\s\S\n]*`

> 先頭の空白文字

`^ `

### REF

- [specs/aozora-text.md at master · aozorahack/specs · GitHub](https://github.com/aozorahack/specs/blob/master/aozora-text.md#%E7%9B%B4%E6%8E%A5%E4%BD%BF%E3%81%88%E3%81%AA%E3%81%84%E4%BD%BF%E3%82%8F%E3%82%8C%E3%81%AA%E3%81%84%E6%96%87%E5%AD%97)

## XHTML

TODO:
