# Tips

## Mapの使い方

- オブジェクトの作成
~~~ java
Map map = new HashMap();
 
//型引数を指定してHashMapクラスのオブジェクトを生成
Map<データ型, データ型> マップ変数 = new HashMap<データ型, データ型>();
~~~

- 値の追加と取り出しはputとgetを使う
~~~ java
map.put(キー名, 値);
  
// 例
map.put("key1", "apple");
System.out.println(map1.get("key1"));
~~~
