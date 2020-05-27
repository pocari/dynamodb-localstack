# README

## sample

```
brew install awscli-local
```

を入れてる前提

### dynamodbのテーブル一覧

```
awslocal dynamodb list-tables
```

### dynamodbのテーブル作成

サンプル

```
awslocal dynamodb create-table --table-name SampleTable --attribute-definitions \
AttributeName=column1,AttributeType=S \
AttributeName=column2,AttributeType=S \
--key-schema \
  AttributeName=column1,KeyType=HASH \
  AttributeName=column2,KeyType=RANGE \
--provisioned-throughput ReadCapacityUnits=5,WriteCapacityUnits=5
```


