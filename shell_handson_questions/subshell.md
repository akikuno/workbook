# サブシェルを使ってみよう

## 問題

- bashの`local`コマンドを使わずにローカル変数を定義してください

- 下記のコマンドをカレントシェルでのディレクトリ移動なしに実行してください

```sh
mkdir -p ./test_TBA/test1/test2/test3
cd  ./test_TBA/test1/test2/test3
echo 'Hello Subshell!' > test.txt
cat test.txt
```

# Enjoy subshell!

## Questions

- Define local variables without using the `local` command of bash

- Execute the following command without moving the directory in the current shell

```sh
mkdir -p ./test_TBA/test1/test2/test3
cd ./test_TBA/test1/test2/test3
echo 'Hello Subshell!' > test.txt
cat test.txt
````