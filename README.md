# check_disk_space
このレポジトリは研究室内のサーバー管理で，各サーバーのdisk spaceを調べて容量が少ない場合に警告を与えるためのテキストを生成するソースコードです．<br>
## 使用方法
以下のコマンドを実行することでdisk spaceの調査を行い，警告を与えるためのテキストを生成します．
```
cd check_disk_space
bash run_check.sh
```
セキュリティの問題で，`server_ips`と`username`と`password`は各自で入力して使用してください．<br>
このコマンドの実行により，`./check_log/{実行日時}`のファイルが作成され，その中に，`check_log_{実行日時}_warnings.txt`と`check_log_{実行日時}.log`が保存されます．
`check_log_{実行日時}_warnings.txt`が実際に使用率の警告閾値(default=85%)を超えるサーバーのipアドレスとディレクトリ名が一覧で保存されます．
`check_log_{実行日時}.log`には，各サーバーのdfコマンドの結果が保存されます．
