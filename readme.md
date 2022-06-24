# オンラインジャッジシステム

- フォームに入力されたコードを実行して解答があっているか判定する。

- 作成したファイルを読み込むにはリフレッシュが必要。

- 固定でよいもの：package名、クラス名、メソッド名（簡単な）
- スレッド5個ぐらい立てて別々に実行

```java
FileReader fr = new FileReader(new File("sample.txt"));
BufferedReader br = new BufferedReader(fr);
String data;
FileWriter outputFile = new FileWriter(new File("c:\\pleiades\\work_for_module\\IO\\src\\io\\CreateOutput.java"));
BufferedWriter bw = new BufferedWriter(outputFile);
StringBuilder sb = new StringBuilder("");
while ((data = br.readLine()) != null) {
	System.out.println(data);
  sb.append(data).append("\n");
}
bw.write(sb.toString());
bw.close();
br.close();
```
