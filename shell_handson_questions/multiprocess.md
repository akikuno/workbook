# コマンドの並列実行

## 問題

- 下記の`sleep`コマンドを並列化してください ('start' -> (sleep x3) -> 'finish')

```sh
echo 'start'
sleep 3
sleep 3
sleep 3
echo 'finish!'
```

- 下記の`sleep`コマンドを**副作用なし**で並列化してください。

＊副作用なし＝標準出力、標準エラー出力、ファイルへのリダイレクトがない状態


```sh
echo 'start'
sleep 3
sleep 3
sleep 3
echo 'finish!'
```

-------------------------------------------------------------------------------
## 解答例

- 下記の`sleep`コマンドを並列化してください ('start' -> (sleep x3) -> 'finish')

```sh
echo 'start'
sleep 3 &
sleep 3 &
sleep 3 &
wait
echo 'finish!'
```

- 下記の`sleep`コマンドを**副作用なし**で並列化してください。

＊副作用なし＝標準出力、標準エラー出力、ファイルへのリダイレクトがない状態

```sh
echo 'start'
{
  sleep 3 &
  sleep 3 &
  sleep 3 &
  wait
} 1>/dev/null 2>&1
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