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

| 常量名       | 常量描述                   |
| ------------ | -------------------------- |
| DT_DEBUG     | 调试模式配置               |
| IN_DESTOON   |                            |
| DT_ADMIN     |                            |
| IN_ADMIN     |                            |
| DT_ROOT      | 根目录                     |
| DT_REWRITE   | 是否路由重写               |
| DT_PATH      |                            |
| DT_STATIC    |                            |
| DT_DOMAIN    |                            |
| DT_WIN       | 是否是WINDOWS系统          |
| DT_CHMOD     |                            |
| DT_LANG      | 语言                       |
| DT_KEY       |                            |
| DT_PRE       |                            |
| DT_EDITOR    |                            |
| DT_CDN       |                            |
| DT_CLOUD_UID |                            |
| DT_CLOUD_KEY |                            |
| DT_CHARSET   |                            |
| DT_CACHE     | 缓存路径                   |
| DT_SKIN      |                            |
| VIP          |                            |
| errmsg       |                            |
| DT_TIME      |                            |
| DT_IP        | 客户端IP                   |
| DT_TOUCH     | 是否是触屏设备             |
| DT_MAX_LEN   |                            |
| DT_MOB       | 判断移动端是 app weixin 等 |
| RE_WRITE     |                            |
| DT_BOT       | 是否是机器 爬虫 蜘蛛       |
|              |                            |

### 常用变量

| 变量      | 描述                       |
| --------- | -------------------------- |
| $DT_PRE   |                            |
| $DT_QST   |                            |
| $DT_TIME  |                            |
| $DT_IP    | 客户端IP                   |
| $DT_URL   | 请求的URL                  |
| $DT_REF   | 请求的来源页               |
| $DT_MOB   | 判断移动端是 app weixin 等 |
| $DT_BOT   | 是否是机器 爬虫 蜘蛛       |
| $DT_TOUCH | 是否是触屏设备             |
| $DT_PC    |                            |

### 其他

- 将GET POST 过来的数据进行处理 以key为变量名 value为变量值进行处理

![1571803254143](./static/image/1571803254143.png)

- cookie 中存有用户的ID信息 需要调用decrypt 函数进行解密

![1571803617895](./static/image/1571803617895.png)

- 数据库中的用户字段可以直接使用 因为

  ![1571810647521](./static/1571810647521.png)





## global.func.php

| 函数名        | 函数功能                                                     |
| ------------- | ------------------------------------------------------------ |
| daddslashes   | 兼容对数组进行addslashes                                     |
| dstripslashes | 兼容对数组进行dstripslashes                                  |
| dtrim         | 去掉字符串内所有空格和其他字符                               |
| dwrite        |                                                              |
| dheader       | 重定向到某个地址                                             |
| dmsg          |                                                              |
| dalert        |                                                              |
| dsubstr       | 截取字符串                                                   |
| cutstr        |                                                              |
| encrypt       | 加密                                                         |
| decrypt       | 解密                                                         |
| mycrypt       | 加解密计算                                                   |
| dround        | 保留几位小数                                                 |
| dalloc        |                                                              |
| strip_nr      |                                                              |
| template      |                                                              |
| ob_template   | ob获取页面内容                                               |
| message       |                                                              |
| login         |                                                              |
| random        | 生成随机字符串                                               |
| set_cookie    | 设置cookie                                                   |
| get_cookie    | 获取指定的cookie                                             |
| get_table     | 获取对应模块ID 的表名                                        |
| get_process   |                                                              |
| send_message  | 发送站内信息                                                 |
| send_mail     | 发邮件                                                       |
| strip_sms     |                                                              |
| send_sms      | 发送短信                                                     |
| send_weixin   | 发送文本消息                                                 |
| word_count    | 计算文本字数 （不确定）                                      |
| cache_read    | 读缓存                                                       |
| cache_write   | 写文件缓存                                                   |
| cache_delete  | 删除缓存                                                     |
| cache_clear   | 清除缓存 文件                                                |
| content_table |                                                              |
| split_table   | 获取当前模块本次要存的表名                                   |
| split_id      | 传入ID 计算拆分的存表的位置                                  |
| ip2area       | 通过Ip获取地理位置                                           |
| banip         | 拦截BAN掉的IP 传入的是黑名单IP列表                           |
| banword       | 过滤非法内容                                                 |
| get_env       | 获取 ip referer self domain scheme port url 信息             |
| convert       | 字符串 编码格式转换                                          |
| get_type      |                                                              |
| get_cat       |                                                              |
| cat_pos       |                                                              |
| cat_url       | 获取分类链接                                                 |
| get_area      | 获取指定区域                                                 |
| area_pos      |                                                              |
| get_maincat   | 获取分类列表                                                 |
| get_mainarea  | 查询区域下的子区域列表                                       |
| get_user      | 获取指定条件查询下的指定字段的用户信息                       |
| check_group   |                                                              |
| tohtml        |                                                              |
| set_style     | 生成一段html元素 可以定义颜色 和 标签                        |
| crypt_action  |                                                              |
| captcha       |                                                              |
| question      |                                                              |
| pages         |                                                              |
| listpages     |                                                              |
| linkurl       |                                                              |
| imgurl        |                                                              |
| userurl       |                                                              |
| useravatar    | 获取用户头像 url                                             |
| userinfo      | 获取用户信息 （内部有缓存优化） 并可指定是否读取缓存数据     |
| userclean     | 清除指定用户的缓存                                           |
| listurl       |                                                              |
| itemurl       |                                                              |
| rewrite       |                                                              |
| timetodate    | 时间戳 转 时间格式 支持指定时间格式                          |
| datetotime    | 字符串转时间戳                                               |
| log_write     | 写日志                                                       |
| load          | 加载文件资源 支持 css js htm缓存 语言包 依赖类库             |
| ad            |                                                              |
| lang          |                                                              |
| check_name    |                                                              |
| check_post    | 检查是否POST请求并且来源合法                                 |
| check_referer | 检查来源页面是否合法                                         |
| is_robot      | 是否是蜘蛛、机器或者爬虫                                     |
| is_ip         | 是否是合法的IP地址                                           |
| is_mobile     | 是否是合法的手机号                                           |
| is_md5        |                                                              |
| is_openid     |                                                              |
| is_touch      | 通过User-agent判断是否是触屏设备                             |
| is_founder    | 是否创始人 （创始人ID设置在 config.inc.php 中 数组下标为 founderid） |
| debug         | 获取运行时长及内存占用信息                                   |
| dhttp         | 设置状态码 及是否立即退出                                    |
| dcurl         | curl请求 支持 GET POST                                       |
| d301          | 301重定向到指定地址                                          |

