# About
[Apache Beam](https://github.com/apache/beam)を使った前処理パイプラインの練習

## GCP Setup
1. サービスアカウントを作成
2. サービスアカウントに権限を付与
3. Credentialを作成しダウンロード
4. key.jsonとしてコンソールに保存
5. 下記を実行してサービスアカウントをアクティベート
```
export GOOGLE_APPLICATION_CREDENTIALS=credential/key.json
gcloud auth activate-service-account --key-file=credential/key.json
```
6.GCSのバケットを作成


## Example

### ex1: pipeline.py
テキストを読み取って単語の数をカウントする  

- 実行方法
GCSのバケットに文章を入力したテキスト(input.txt)を保存する。  
`yourstoragename``とyourregion`は適宜変更する

```python
poetry run python src/pipeline.py --input=gs://yourstoragename/input.txt --output=gs://yourstoragename/output.txt --region yourregion
```