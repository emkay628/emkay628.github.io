# Object Calisthenics
*9 Steps to Better Software Design Today by Jeff Bay*
  
## 9つの手順
1. One level of indentation per method
    1. ガード節
    2. メソッド抽出
    3. ポリモーフィズムの分岐置換
    4. Null Object / Optional
    5. ルール5に同じ。デメテルの法則を参照せよ
2. Don’t use the ELSE keyword
    1. ルール1に同じ。とくにガード節を用いよ
3. Wrap all primitives and Strings
    1. `int age` ではなく、`Age` 型を作れ
    2. 要素をラップせよ
4. First-class collections
    1. コレクションをラップせよ
    2. 要素に続き、集合もラップせよ
5. One dot per line
    1. OK: `object.methodA();`
    2. NG: `object.methodA().methodB()...;`
6. Don’t abbreviate
    1. 名前を略すな
    2. 名前が長くなるならば、責務を分割せよ
    3. よい命名の7原則を参照せよ
7. Keep all entities small
    1. パッケージ: 10ファイル以内
    2. クラス: 50行以内
    3. メソッド: 10行以内
8. No class with more than two instance variables
    1. ルール3を参照せよ
    2. ルール4を参照せよ
    3. クラスを分割せよ
9. No getters/setters/properties
    1. データを晒すな。ふるまいで語れ

## 具体的なテクニック
ガード節 - guard clause

- `if` 文と、早期脱出 (early exit:`return/continue/break`) を組み合わせて使う
- 例外系や異常系などを早期に除き、正常系を安全に処理する
- メソッドやループのはじめに記述する

メソッド抽出 - Extract Method

- つまり、メソッドを分けよ、ということ

ポリモーフィズムの分岐置換

- `if/switch` の条件分岐を、ポリモーフィズムに置換せよ

Null Object / Optional

- `if` 文で`null` を判断するな (増殖させるな)
- `null` という「存在しないこと」や「何もしないこと」をオブジェクトとして表現せよ

## 表にして分類する
| 層 | 目的 | ルール |
| --- | --- | --- |
| 1. 構文層<br>→ 構造を浅くする | ネスト、分岐、依存を断つ | #1, #2, #5 |
| 2. 設計層<br>→ 意味を分ける | データを語彙として扱う | #3, #4, #6 |
| 3. 構造層<br>→ 全体を小さくする | クラス、モジュール単位の整理 | #7, #8, #9 |

## まとめ
### オブジェクト (指向) とは

- 人間中心主義である
- データ構造ではない
- 要素と演算が閉じている数学的構造である


## 頭の中の概念の整理
| 静 | 動 |
| :---: | :---: |
| 状態 | 動作 |
| 形式 | 意味 |
| 要素 | 演算 |
| 属性 | 操作 |
| データ | メソッド |
| 値 | 関数 |
| プロパティ | プロシージャ |
| 効率 | 責任 |
| つくり | はたらき |

## 参考文献
- ThoughtWorksアンソロジー ―アジャイルとオブジェクト指向によるソフトウェアイノベーション [https://amzn.asia/d/h9hqzKd](https://amzn.asia/d/h9hqzKd)
- オブジェクト指向が苦手なあなたが今日から始められる練習方法を紹介します【オブジェクト指向エクササイズ】 [https://youtu.be/Ucd-lMmDuFQ?si=ei2afnO_xVBHclt3](https://youtu.be/Ucd-lMmDuFQ?si=ei2afnO_xVBHclt3)

## 関連項目

- ドメイン駆動設計
- クリーンアーキテクチャ
