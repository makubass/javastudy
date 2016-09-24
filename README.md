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
※「\」は「￥（小文字の円マーク）」と読み替えて。  

プロジェクト「chap17」、パッケージ「sample」と作った。  
ディレクトリはこうなる　c:\myspace\chap17\sample  
クラス名をRunTestとしてソースを書いて保存するとこうなる。

``` 
C:\myspace\chap17\sample
	|---RunTest.java
```

コンパイルする。
```
C:\myspace\chap17>Javac sample/Runtest.java
```

するとクラスファイルが生成される。  
``` 
C:\myspace\chap17\sample
	|---RunTest.java
	|---RunTest.class
```

で、確認のためにsampleディレクトリに移動したのがハマりの始まり。  
```
C:\myspace\chap17>cd sample
C:\myspace\chap17\sample>dir
		RunTest.java
		RunTest.class
```

そのまま実行すると・・・  
C:\myspace\chap17\sample>Java RunTest  
「エラー：メインクラスが見つからなかったかロードできませんでした」  

dirで確認したのはいいのだが、そのままsampleディレクトリで実行してしまった。   java実行するためにはプロジェクトのフォルダをカレントディレクトリにし、
パッケージを指定したかたちで実行する必要があった。  

```
C:\myspace\chap17
