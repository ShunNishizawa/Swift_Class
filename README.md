# Swift_Class

## クラス
- クラスのインスタンスは参照型
- 構造体はひとまとまりの意味のあるデータを実現するために使い、クラスはシステムを構成する構造や、役割を与えられて動作する能動的な単位を実現するために使われる
- クラスでは全項目イニシャライザは使えない

## 継承
- 別のクラスの実装を利用して、同様な記述を繰り返すことなく新しいクラスを定義できる仕組み
- 定義を引き継いで新たに手木されるクラスをサブクラス、定義を参照される側のクラスをスーパークラスと呼ぶ
- スーパークラスを指定せずにクラスを定義でき、そのようなクラスをベースクラスという
- イニシャライザは継承できない（ある条件のもとでは可能）
- スーパークラスのメソッドを上書き（オーバーライド）することができ、その際はメソッドの先頭に```override```を記述する
- スーパークスラスの定義であることを示すには```super```というキーワードを使う

```
// スーパークラスの定義例
class クラス名: スーパークラス名, プロトコル1, プロトコル2, ...
```

## 簡易イニシャライザ(convenience initializer)
- 他のイニシャライザを呼び出して実行できる
- 呼び出し側をコンビニエンスイニシャライザ、呼び出される側を指定イニシャライザ
- 直接あるいは間接的に指定イニシャライザを呼び出さないといけない
- 簡易イニシャライザはスーパークラスのイニシャライザを呼び出してはいけない
- ```convenience```というキーワードをつける

```
// 定義例
convenience init(仮引数) {
	~
}
```
