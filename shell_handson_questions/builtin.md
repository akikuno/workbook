# ビルトインコマンドと外部コマンドの速度の違いをしろう

## 問題

（おそらく）お手持ちの環境には2種類のechoが存在します。  
`/bin/echo`と`echo`です。  

- それぞれの`echo`を用いて`echo hoge > /dev/null`を1000回実行し、その計算時間を記録してください。

- どちらかが遅いと思いますが、その理由を考察してください。

# Recognize the difference between the speed of built-in commands and external commands

## Questions

There are (probably) two types of echoes in your environment.  
`/bin/echo` and `echo`.  

- Run `echo hoge > /dev/null` 1000 times with each `echo` and record the computation time.

- Consider the reasons why one of them is slower than the other.