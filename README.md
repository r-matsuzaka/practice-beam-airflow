# About
[Apache Beam](https://github.com/apache/beam)を使った前処理パイプラインの練習

## GCP Setup
1. サービスアカウントを作成
2. サービスアカウントに権限を付与
3. Credentialを作成しダウンロード
4. key.jsonとしてコンソールに保存
vimで貼り付けるときは`:set paste`で自動インデントを回避できる

5. 下記を実行してサービスアカウントをアクティベート
```python
export GOOGLE_CLOUD_PROJECT=key.json
gcloud auth activate-service-account --key-file=key.json
```

6. 下記を実行(東京:asia-northeast1の場合)
```python
python pipeline.py --input=gs://yourstoragename/input.txt --output=gs://yourstoragename/output.txt --region asia-northeast1
```