# OAuth2令牌校验实验

## 一、先决条件

通过lab03/04/05/06其中一个获取访问令牌(access token)

## 二、校验令牌

Postman请求：

```
curl -X POST --user test_client_2:test_secret http://localhost:8080/v1/oauth/introspect -d "token=00ccd40e-72ca-4e79-a4b6-67c95e2e3f1c&token_type_hint=access_token"
```

响应案例：

```json
{
  "active": true,
  "scope": "read_write",
  "client_id": "test_client_1",
  "username": "bobo@spring2go.com",
  "token_type": "Bearer",
  "exp": 1454868090
}

```



