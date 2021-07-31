# ciba-test

## 環境構築
```bash
user@host: ~/workspace $ docker compose up -d
user@host: ~/workspace $ open http://localhost:8088/
```

`taro`というユーザーを手動で作成する

## CIBAフロー

```bash
curl -X POST \
   -H "Content-Type:application/x-www-form-urlencoded" \
   -H "Authorization:Basic dGVzdC1jbGllbnQ6MmFlNmQ4MWQtYmM3OC00MzRlLWE3YjgtOTg1OTIxZTBkNDdi" \
   -d "scope=openid" \
   -d "login_hint=taro" \
   -d "binding_message=hogehuga" \
 'http://localhost:8088/auth/realms/SampleRealm/protocol/openid-connect/ext/ciba/auth'

```