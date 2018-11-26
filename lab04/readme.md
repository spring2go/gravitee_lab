# OAuth2简化模式实验

## 一、获取访问令牌

浏览器请求：

```
http://localhost:8080/web/authorize?client_id=test_client_1&redirect_uri=http://www.example.com&response_type=token&state=somestate&scope=read_write
```

根据页面提示认证和授权客户应用

响应案例：

```
https://www.example.com/#access_token=087902d5-29e7-417b-a339-b57a60d6742a&expires_in=3600&scope=read_write&state=somestate&token_type=Bearer
```






















