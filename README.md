# swagger


## openapi.yaml
APIの仕様書


## swagger-editor
https://swagger.io/tools/swagger-editor/ のローカル版


## swagger-ui
http://dev-host.local:19882/

openapi.yamlをweb上でドキュメント化できる

## stoplight/prism:3 
APIモック

GETサンプル
```

curl http://localhost:19883/colors | jq


# レスポンス
{
  "message": 200,
  "colors": [
    {
      "id": 1,
      "name": "赤",
      "created_at": "2002/05/12 20:30:15",
      "updated_at": "2002/05/12 20:30:15"
    }
  ]
}

```

POSTサンプル
```
curl http://localhost:19883/colors  -X POST -H "Content-Type: application/json"  -d '{"name": "赤"}' | jq .

＃レスポンス
{
  "message": "Success",
  "color": {
    "id": 1,
    "name": "赤",
    "created_at": "2002/05/12 20:30:15",
    "updated_at": "2002/05/12 20:30:15"
  }
}

```