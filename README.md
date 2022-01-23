# test-dataflow
Dataflowを使った前処理パイプラインの練習
Cloud Composerで定期実行させる

## GCP Setup
GCPコンソール上で実行を想定  
1. サービスアカウントを作成
2. 下記のサービスアカウントに権限を付与
- 
3. Credentialを作成しダウンロード
4. key.jsonとしてコンソールに保存
vimで貼り付けるときは`:set paste`で自動インデントを回避できる

5. 下記を実行してサービスアカウントをアクティベート
```python
export GOOGLE_CLOUD_PROJECT=key.json
gcloud auth activate-service-account --key-file=key.json
```
