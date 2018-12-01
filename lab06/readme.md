# OAuth2客户端模式实验

## 一、获取访问令牌

Postman请求：

```
curl -X POST --user test_client_1:test_secret http://localhost:8080/v1/oauth/tokens -d "grant_type=client_credentials&scope=read_write"
```

响应案例：

```json
{
  "access_token": "00ccd40e-72ca-4e79-a4b6-67c95e2e3f1c",
  "expires_in": 3600,
  "token_type": "Bearer",
  "scope": "read_write"
}
```

## 二、参数

https://tools.ietf.org/html/rfc6749#section-4.4























