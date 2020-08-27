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

openAPIをjsonにしてaws-cliで１APIGatewayを作れる

YamlからJSONに変換
https://www.convertjson.com/yaml-to-json.htm

```
#カレントディレクトにopenapi.jsonをおいて下記コマンドを実行(APIgatewayが作られる)
aws apigateway import-rest-api --body 'file://openapi.json' --region us-east-1

#レスポンス
{
    "id": "nmqtd5bbnc",
    "name": "OpenAPIテスト",
    "description": "OpenAPIテスト",
    "createdDate": 1598531567,
    "version": "1.0.0",
    "warnings": [
        "Parse issue: attribute paths.'/area/{zipCode}'(get).parameters.[zipCode].type is unexpected",
        "More than one server provided. Ignoring all but the first for defining endpoint configuration"
    ],
    "apiKeySource": "HEADER",
    "endpointConfiguration": {
        "types": [
            "EDGE"
        ]
    }
}
```