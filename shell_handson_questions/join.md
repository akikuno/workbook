# Shellコマンドでテーブル結合をしよう！

## ファイルの用意

```sh
cat << EOF > list1.txt
id name
1 aka
2 ao
3 shiro
4 kuro
5 ichiro
EOF

cat << EOF > list2.txt
id name
1 ichiro
2 jiro
3 saburo
5 goro
EOF
```

## 問題

- `list1.txt`と`list2.txt`をID列をキーとして内部結合してください

- `list1.txt`と`list2.txt`をlist1.txtのID列, list2.txtのname列をキーとして内部結合してください

- `list1.txt`と`list2.txt`をlist1.txtのID列をキーとして外部結合してください

- `list1.txt`と`list2.txt`を全結合してください

# Let's do a table join with the Shell command!

## Questions

- Inner join `list1.txt` and `list2.txt` with the ID sequence as a key.

- Inner join `list1.txt` and `list2.txt` with the ID column of list1.txt and the name column of list2.txt as a key.

- Outer join `list1.txt` and `list2.txt` with the ID sequence of list1.txt as a key.

- Full join `list1.txt` and `list2.txt` into a single file.
