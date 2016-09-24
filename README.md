# javastudy
javaでプログラミングを勉強したことで後で参考にしたいものをメモ。  

* 1からnの整数乱数を取得する  
`Math.random()`
は0以上、1未満の乱数を返す。  
n倍して1を足すと、1以上n+1未満の乱数乱数になる。  
但し、戻り値はdoubleなので、キャストして小数点以下を切り捨てる切り捨てる。

```java:random
int r = (int)(Math.random() * n + 1);
```
  
* nullか空文字""かをチェックするisEmptyメソッド
```
public static boolean isEmpty(String str){
	if(str==null || str.equals("")){
		return true;
	}else
		return false;
	}
```

* コマンドでのコンパイルと実行で困ったこと。  
*「\」は「￥（小文字の円マーク）」と読み替えて。
c:\
