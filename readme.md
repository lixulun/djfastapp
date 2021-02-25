# Django快速原型开发模板 djfastapp

面向快速APP原型测试开发，迅速实现一个创意。有的开源项目是为开发者提供现成的解决方案，有的开源作品属于村上春树所称作的“私人性质”，主要目的不是吸引别人来使用，但还是可以给别人带来启发。本项目属于后者。

指导思想是：
- 不随意改变Django的约定；
- 牺牲一部分Django的默认安全策略以换取开发效率；
- 面向内部用户。

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
* 配置static在非调试环境运行
* 默认语言改从en-us改成zh-Hans

## 解释

* 默认使用时区（USE_TZ=True），这是Django官方推荐的行为。使用django.utils.timezone包代替datetime包，请[参考文档](https://docs.djangoproject.com/en/2.2/topics/i18n/timezones/)
