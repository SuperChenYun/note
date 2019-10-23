# Destoon笔记

## common.inc.php 

### common.inc.php 引入的文件有

- /include/rewrite.inc.php
- /config.inc.php
- /include/global.func.ph
- /include/tag.func.php
- /api/im.func.php
- /api/extend.func.php
- /lang/{$lang}/lang.inc.php
- /include/db{$DB_TYPE}.class.php
- /include/cache_{$CACHE_TYPE}.class.php
- /incldue/session_{$SESSION_TYPE}.class.php
- /include/file.func.php



### common.inc.php 定义及使用的常量有

| 常量名     | 常量描述          |
| ---------- | ----------------- |
| DT_DEBUG   | 调试模式配置      |
| IN_DESTOON |                   |
| DT_ADMIN   |                   |
| IN_ADMIN   |                   |
| DT_ROOT    | 根目录            |
| DT_REWRITE | 是否路由重写      |
| DT_PATH    |                   |
| DT_STATIC  |                   |
| DT_DOMAIN  |                   |
| DT_WIN     | 是否是WINDOWS系统 |
| DT_CHMOD   |                   |
| DT_LANG    | 语言              |
| DT_KEY     |                   |
| DT_CHARSET |                   |
| DT_CACHE   | 缓存路径          |
| DT_SKIN    |                   |
| VIP        |                   |
| errmsg     |                   |
| DT_TIME    |                   |
| DT_IP      |                   |
| DT_URL     |                   |
| DT_REF     |                   |
| DT_MOB     |                   |
| DT_BOT     |                   |
| DT_TOUCH   |                   |
| DT_PC      |                   |



### 其他

- 将GET POST 过来的数据进行处理 以key为变量名 value为变量值进行处理

![1571803254143](./static/image/1571803254143.png)

- cookie 中存有用户的ID信息 需要调用decrypt 函数进行解密

![1571803617895](./static\image\1571803617895.png)