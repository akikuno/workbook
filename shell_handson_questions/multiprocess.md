# スクリプトをマルチプロセスで動かそう！

## 問題

- 下記の`sleep`コマンドを**並列化**してください

```sh
sleep 3
sleep 3
sleep 3
```

- 下記の`sleep`コマンド**のみ**を並列化してください

```sh
echo 'start'
sleep 3
sleep 3
sleep 3
echo 'finish!'
```

- 下記の`sleep`コマンド**のみ**を**副作用なし**で並列化してください。

＊副作用なし＝出力なし（標準出力、標準エラー出力、ファイルへのリダイレクト）

```sh
echo 'start'
sleep 3
sleep 3
sleep 3
echo 'finish!'
```

# Enjoy multiprocess!

## Questions

- Parallelize the following `sleep` command

```sh
sleep 3
sleep 3
sleep 3
```

- Parallelize the following only `sleep` command

```sh
echo 'start'
sleep 3
sleep 3
sleep 3
echo 'finish!'
```

- Parallelize the following only `sleep` command with **no side effects**.

* No side-effects means no output (standard output, standard error, redirect to file).

```sh
echo 'start'
sleep 3
sleep 3
sleep 3
echo 'finish!'
```