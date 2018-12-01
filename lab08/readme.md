# OAuth2令牌刷新实验

## 一、先决条件

通过lab03/05其中一个获取刷新令牌(refresh token)

## 二、刷新令牌

Postman请求：

```
curl -X POST --user test_client_1:test_secret http://localhost:8080/v1/oauth/tokens -d "grant_type=refresh_token&refresh_token=6fd8d272-375a-4d8a-8d0f-43367dc8b791"
```

响应案例：

```json
{
  "user_id": "6e718e4e-3b17-4cf3-bccd-4b6ee31957c8",
  "access_token": "1f962bd5-7890-435d-b619-584b6aa32e6c",
  "expires_in": 3600,
  "token_type": "Bearer",
  "scope": "read_write",
  "refresh_token": "3a6b45b8-9d29-4cba-8a1b-0093e8a2b933"
}

```

## 三、参考

https://tools.ietf.org/html/rfc6749#section-6



