# new-mail
创建一个任意地址的邮箱服务，转发到钉钉


## 域名解析配置

```
记录类型    主机记录      记录值
A             mx        x.x.x.x
MX            *         mx.example.com
A             @         x.x.x.x
```

## 服务启动

- 不设置通知直接启动
```
./new-mail
```

- 环境变量方式
```
export DINGTALK_ACCESS_TOKEN=xxxxx
export DINGTALK_SECRET=xxxxx
./new-mail
```

- 参数方式
```
./new-mail -dt xxxxx -ds xxxxx
```


## 计划

[x] 接受邮件, 打印
[] 通知
    [x] 发送到钉钉机器人
    [ ] 发送到微信
[ ] 配置文件
[ ] 日志记录
[ ] 数据存储到数据库
[ ] Web 页面
    [ ] 登录页面
    [ ] 邮件列表
    [ ] 邮件详情
    [ ] 邮件转发


## 参考

> [Maddy 自建邮件服务](https://axionl.me/p/maddy-%E8%87%AA%E5%BB%BA%E9%82%AE%E4%BB%B6%E6%9C%8D%E5%8A%A1/)

> [crazy-email-recv-srv](https://github.com/xjjdog/crazy-email-recv-srv)

## 引用

> [go-smtp](github.com/emersion/go-smtp)

> [pmsg](github.com/lenye/pmsg)
