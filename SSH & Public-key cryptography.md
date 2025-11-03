# SSHとは
SSH: Secure Shell とは、ネットワーク上のリモートコンピューターに安全に接続、操作する通信プロトコルである。公開鍵暗号方式などを利用して、ユーザー認証を行う。

# 公開鍵暗号方式

| 公開鍵 | 秘密鍵 |
| :---: | :---: |
| 拡張子 <br> .pub | 拡張子 <br> なし |

公開鍵
```
ssh-ed25519 AAAA...fake...key example@localhost
```
```
ssh-rsa AAAA...fake...key example@localhost
```

秘密鍵
```
-----BEGIN OPENSSH PRIVATE KEY----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACCfakeFAKEfakeFAKEfakeFAKEfakeFAKEfakeFAKEfakeFAKEAAAAC3NzaC
1lZDI1NTE5AAAAICfakeFAKEfakeFAKEfakeFAKEfakeFAKEfakeFAKEfakeFAKE
-----END OPENSSH PRIVATE KEY-----
```
```
-----BEGIN RSA PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACCfakeFAKEfakeFAKEfakeFAKEfakeFAKEfakeFAKEfakeFAKEAAAAC3NzaC
1lZDI1NTE5AAAAICfakeFAKEfakeFAKEfakeFAKEfakeFAKEfakeFAKEfakeFAKE
```
> [!NOTE]
> これらの鍵は学習用のサンプルである。よって実際の接続には使えない。

# 運用例
- 一つの端末 = 一つのOS
- 一つのOSはかならず一人以上のユーザーを含む
- 公開鍵と秘密鍵は一対一の組み合わせとして扱う

以上の3つから、次のことが言える。

-  一つの端末 = 一つのOS = 一人のユーザー = 一組の鍵

SSHの場合、接続する側もされる側もこの原則が適用されるべきである。



