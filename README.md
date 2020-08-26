# swagger


## openapi.yaml
APIの仕様書


## swagger-editor
https://swagger.io/tools/swagger-editor/ のローカル版

http://dev-host.local:19881/

## swagger-ui
http://dev-host.local:19882/

openapi.yamlをweb上でドキュメント化できる

## stoplight/prism:3 
APIモック

GETサンプル
```

curl http://localhost:19883/xxxx | jq


# レスポンス
```

POSTサンプル
```
curl http://localhost:19883/XXXXX -X POST -H "Content-Type: application/json"  -d '{"key": "value"}' | jq .

＃レスポンス

```
