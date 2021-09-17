# mokuroku-spec
「地理院タイル目録」は地理院タイル一枚一枚の所在情報を記述したファイルです。  
「地理院タイル目録」の仕様は次のとおりです。

# ファイル内容
```csv
（パス）,（最終更新時刻）,（サイズ）,（MD5SUM）
```
1. 最終更新時刻(mtime)は、UNIX起算時を整数化したものとしています。
2. パスからURLへの換算は、https://cyberjapandata.gsi.go.jp/xyz/{t}/（パス） です。

例：https://cyberjapandata.gsi.go.jp/xyz/std/18/239192/93905.png に対する地理院タイル目録のレコードは、次の通りとなります（平成２７年１月現在）。
```csv
18/239192/93905.png,1409468135,285,1635de9ccf8ec5d7e71ce535b72e1a23
```
# URL
「地理院タイル目録」のURLは、次のとおりです。
```
https://cyberjapandata.gsi.go.jp/xyz/{t}/mokuroku.csv.gz
```

# 留意点
- 地理院タイル目録は、サーバ管理の都合上、予告なく提供を中断する場合があります。
- 地理院タイルサーバの帯域は有限な資源です。利用にあたっては有意義に活用いただくことをお願いいたします。キャッシュいただいたタイルの一つ一つが、平均的に1回以上は実際に使用されることが、キャッシュいただく場合の目安であると考えていただければ幸いです。
- 令和2年12月現在、{t}がstd、pale、englishのみ定期的に更新しております。毎月10日までに公開し、前月末時点の情報が記載されています。

# See Also
- [地理院タイルダウンロードツール](https://github.com/gsi-cyberjapan/tdlmn)

# 履歴
地理院タイル目録は、2015年2月4日の第2回地理院地図パートナーネットワーク会議でリリースされました。
