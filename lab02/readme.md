# 起步准备实验

## 一、安装MySql

### 安装

下载[MySQL Community(5.6.x)+Workbench](https://dev.mysql.com/downloads/mysql/)，按照提示进行本地安装即可。

### 创建数据库

打开MySQL Workbench，通过`Navigator`鼠标右键菜单`Create Schema...`添加数据库**gravitee**

## 二、构建gravitee

在%GOPATH%/src/github.com/spring2go/gravitee目录中，构建gravitee oauth2服务器应用

```
go build gravitee-server.go
```

检查当前目录生成生成`gravitee.exe`

## 三、生成数据库表

在%GOPATH%/src/github.com/spring2go/gravitee目录中

根据数据库配置调整默认配置文件`config.xml`中用户名和密码，其它参数可用缺省

运行**migrate**生成数据库表

```
gravitee migate
```

通过mysql workbench检查下列表格已经成功创建：

* oauth_clients
* oauth_users
* oauth_scopes
* oauth_roles
* oauth_access_tokens
* oauth_refresh_tokens
* oauth_auhtorization_codes
* migrations

## 四、添加种子数据

在%GOPATH%/src/github.com/spring2go/gravitee目录中

运行**loaddata**加载种子数据

```
gravitee loaddata oauth/fixtures/scopes.yml oauth/fixtures/roles.yml oauth/fixtures/test_clients.yml oauth/fixtures/test_users.yml
```

通过mysql workbench检查下列表格中已经有种子数据：

* oauth_clients
* oauth_users
* oauth_scopes
* oauth_roles


















