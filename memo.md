# js sample

## memo
```ruby
def sample
	text = "text text"
end

puts sample
```

``` python
text = "sample"
print text
```

```javascript
let text = "text";

console.log(text);
```

---

### function

- 命名規則
	- '動詞 + 名詞'のように付けて
	- 例えば -> function drinkCaffee();

- 関数コンストラクタ
	- 関数リテラル/コンストラクタで定義した場合は実行時に評価される
		- つまり関数を実行より前に記述しなければならない

```javascript
var hoge = new Function(hoge01, hoge02,hoge03);

```
- メリットとしては引数や関数を文字列として定義できる
- ただし乱用は禁物

- リテラル:データ型に格納できる値そのもの
- オブジェクトリテラル:名前をキーにアクセスできる配列みたいなもの
- 例えば配列だと ary[0, 1, 2, 3]
- オブジェクトは obj {name0: 0, name1: 1, name2: 2, name3: 3}
- こういうこと！？なお呼び出すときは↓
- array -> ary[2];
- object -> obj.name2; obj.['name2'];
- 関数もデータ型の一種

---

### variables scopes

- わかりきってることだけど関数の中で宣言された変数のスコープはその関数の中だけ
	- 基本的にグローバル変数は害悪や!
	- local変数は関数の最初に定義しておくこと!(詳しくはsample.jsのVARIABLES参照)
	- localではvarは必須やで
	- ES6ではletとかconstとか使える

- 基本型と参照型
	- 基本は関数の引数でその関数外で宣言された変数と同名の変数を定義しても別物として認識されるが
	- 実行時の関数の引数としてグローバルの変数が呼ばれた場合は参照しているメモリの場所が等しくなる為、結果的に代入されることになる(詳しくはsample.jsのFUNCTION参照)

---

### criate caluculator

- 1.DOM定義
- 2.ボタンごとに挙動を設定
	- 数値の場合
		- 押されたボタンのvalueをlineに表示
		- 1~9は数値を返す
	- 演算子の場合
		- 前の入力が数値の場合に走る
		- eval()で計算!
		- lineを消去後、totalに格納してlineに表示
	- "="の場合
		- 合計をクリア、演算子をリセット
		- 演算子を退避
	- "C"の場合
		- all clear
		- 0を表示(totalをリセット、表示)
