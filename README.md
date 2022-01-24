# About

[Apache Beam](https://github.com/apache/beam) と [Apache Airflow](https://github.com/apache/airflow) の練習

## GCP Setup
1. サービスアカウントを作成
2. サービスアカウントに権限を付与
3. Credentialを作成しダウンロード
4. `credential`直下にkey.jsonを保存
5. 下記を実行してサービスアカウントをアクティベート
```
export GOOGLE_APPLICATION_CREDENTIALS=credential/key.json
gcloud auth activate-service-account --key-file=credential/key.json
```
6.GCSのバケットを作成


## Beam Example

### ex-b1:
テキストを読み取って単語の数をカウントする  

**実行方法**  
GCSのバケットに文章を入力したテキスト(input.txt)を保存する。  
`yourstoragename`と`yourregion`は適宜変更する。

```python
poetry run python src/pipeline_ex-b1.py --input=gs://yourstoragename/input.txt --output=gs://yourstoragename/output.txt --region yourregion
```

### ex-b2:


## Airflow Example

### ex-a1:
airflowディレクトリへpathを通す。  
```
export AIRFLOW_HOME=path_to_airflow
```

```
airflow dags backfill hello_world     --start-date 2022-01-26     --end-date 2022-01-26
```