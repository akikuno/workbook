# 意外とむずかしい？塩基配列処理に挑戦しよう！

## 問題

ここに塩基配列`ACGTAAAAAACCCCCTTTTTTTTTTGG`があります。

- 逆相補鎖`CCAAAAAAAAAAGGGGGTTTTTTACGT`を得るシェルスクリプトを書いてください
- リピート配列をマスクした結果`ACGTaaaaaaCCCCCttttttttttGG`を得るシェルスクリプトを書いてください
  - なお、ここではリピート配列を**6つ以上連続する同一塩基**と定義します

# Let's try to manipulate sequence data!

## Questions

Here's the sequence `ACGTAAAAAACCCCCCCTTTTTTTTTTTTGG`.

- Write a script to get the reverse complementary as `CCCAAAAAAAAGGGGGTTTTTTACGT`

- Write a shell script to get the result of masking the repeat array as `ACGTaaaaaaCCCCCttttttttttGG`.
  - A repeat sequence is defined here as **6 or more consecutive identical bases**.