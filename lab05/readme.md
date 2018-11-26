# OAuth2用户名密码模式实验

## 一、获取访问令牌

Postman请求：

```
curl -X POST --user test_client_1:test_secret http://localhost:8080/v1/oauth/tokens -d "grant_type=password&username=bobo@spring2go.com&password=test_password&scope=read_write"
```


响应案例：

```json
{
  "user_id": "6e718e4e-3b17-4cf3-bccd-4b6ee31957c8",
  "access_token": "00ccd40e-72ca-4e79-a4b6-67c95e2e3f1c",
  "expires_in": 3600,
  "token_type": "Bearer",
  "scope": "read_write",
  "refresh_token": "6fd8d272-375a-4d8a-8d0f-43367dc8b791"
}
```






















