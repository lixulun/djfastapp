# Django快速原型开发模板 djfastapp

面向快速APP原型测试开发，迅速实现一个创意。指导思想是，不随意改变Django的约定，牺牲一部分Django的默认安全策略以换取开发效率。非面向终端用户。

## 使用方法

```
django-admin startproject --template https://github.com/lixulun/djfastapp/archive/master.zip fastapp1
```
这条命令会创建一个fastapp1目录，使用djfastapp模板

## 与默认模板的不同
* 默认创建APP，名字为app，与配置文件夹合并
* 时区默认改为Asia/Shanghai
* 去掉了csrf中间件
* ALLOWED_HOSTS不做限制

## 解释

* 不关闭时区支持的原因。Django官方推荐[打开时区](https://docs.djangoproject.com/en/2.2/topics/i18n/timezones/#setup)。我的理由是使用官方指导，避免aware/naive datetime对象的混用会避免很多麻烦。方法请[参见文档](https://docs.djangoproject.com/en/2.2/topics/i18n/timezones/)