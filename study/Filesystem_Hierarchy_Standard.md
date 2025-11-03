# まえがき
サーバーのディレクトリ構造の仕組みを知りたい。バージョンやディストリビューションに共通の構造がある、と予想した。

# FHSとは
Filesystem Hierarcy Standard の略である。実質的に、Linux Foundation が管理している。

# 共有可能性と変更可能性
ファイルをこの2つの軸を交えて管理する。

||shareable<br>(共有)|unshareable<br>(占有)|
| :-: | :-: | :-: |
|variable<br>(動的)|||
|static<br>(静的)|||

## 参考
Chapter 2. The Filesystem https://refspecs.linuxfoundation.org/FHS_3.0/fhs/ch02.html

# 構造
## ルート
`/`<br>
ここからすべてがはじまる
## 必須ディレクトリ
/bin

# 参考文献
Filesystem Hierarchy Standard
https://refspecs.linuxfoundation.org/FHS_3.0/fhs/index

# あとがき