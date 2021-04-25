# 初心者向け

## 対象者レベル

- ターミナルを起動できる
- (オプション) [BED](https://m.ensembl.org/info/website/upload/bed.html)を知っている

## 準備

以下のコードを実行してください  
（意味はわからなくて大丈夫です。知りたい方は`ヒアドキュメント shell`でググってください。）

```sh
TAB="$(printf '\t')"

cat << EOF > test.bed
1${TAB}100${TAB}1000${TAB}geneA${TAB}20
1${TAB}100${TAB}1000${TAB}geneA${TAB}200
1${TAB}900${TAB}2000${TAB}geneB${TAB}100
1${TAB}1000${TAB}2200${TAB}geneB${TAB}10
2${TAB}100${TAB}1500${TAB}geneC${TAB}1000
10${TAB}100${TAB}1000${TAB}geneD${TAB}2000
1${TAB}100${TAB}1000${TAB}geneA${TAB}200
EOF
```


## 問題

### 環境確認

- `pwd`を実行してください
- `ls`を実行してください

### ディレクトリ移動

- `mkdir test_insilico`を実行し、その後`ls`を実行してください
- `cd test_insilico`を実行し、その後`pwd`を実行し、その後`ls`を実行してください
- `cd ../`を実行し、その後`pwd`を実行し、その後`ls`を実行してください
- `rm -rf test_insilico`を実行し、その後`ls`を実行してください

### I/O

- `test.bed`をすべて表示してください (`cat`)
- 先頭から3行を表示してください (`head`)
- 行末から2行を表示してください (`tail`)
- 先頭から3行を表示して、行末から2行を表示してください（`head`, `tail`, `|`: パイプ）
- 先頭から3行を表示して`test2.bed`に保存してください (`head`, `>`:入出力リダイレクト)

### sort, uniq

- 1列目を基準に辞書順にソートしてください (`sort`)
- 1列目を基準に数字順にソートしてください (`sort -n`)
- 5列目を基準に数字順にソートしてください (`sort -k`)
- 重複行を削除してください  (`sort -u`)
- 重複行の数を表示してください (`sort`, `uniq -c`)

### grep

- `geneB`の行を表示してください (`grep`)
- `geneB`の行**以外**を表示してください (`grep -v`)
- `geneA`と`geneB`の行を表示してください (`grep -e`)
- `geneA`と`geneB`の行を表示して、かつスコアが`20`の行を表示してください (`grep -e`, `|`)

### sed

- `gene`を`Gene`に置換してください (`sed`)
- 1列目の行頭に`chr`をつけてください (`sed`, 正規表現)
- タブ区切りをコンマ区切りに変換してください (`sed`, エスケープシークエンス)