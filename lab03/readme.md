# OAuth2授权码模式实验

## 一、获取授权码

浏览器请求：

```
http://localhost:8080/web/authorize?client_id=test_client_1&redirect_uri=http://www.example.com&response_type=code&state=somestate&scope=read_write
```

根据页面提示认证和授权客户应用


响应案例：

```
https://www.example.com/?code=7afb1c55-76e4-4c76-adb7-9d657cb47a27&state=somestate
```

## 二、获取访问令牌

Postman请求：

```
curl -X POST --user test_client_1:test_secret http://localhost:8080/v1/oauth/tokens -d "code=7afb1c55-76e4-4c76-adb7-9d657cb47a27&grant_type=authorization_code&redirect_uri=https://www.example.com&scope=read_write"

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

## 三、参考

https://tools.ietf.org/html/rfc6749#section-4.1























