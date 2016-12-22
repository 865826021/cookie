# Cookie管理
组件提供了高效、安全的cookie管理机制，每一个储存到客户端的cookie数据均经过安全加密处理极大的提高了系统安全性。
登录 [GITHUB](https://github.com/houdunwang/cookie)  查看源代码

[TOC]
#开始使用

####安装组件
使用 composer 命令进行安装或下载源代码使用。

```
composer require houdunwang/cookie
```
> HDPHP 框架已经内置此组件，无需要安装

####配置
配置主要是设置加密Cookie使用的密钥, 如果不执行配置系统将使用默认密钥。
```
$config = [
	//cookie加密密钥
	'secureKey' => 'houdunwang88'
];
\houdunwang\config\Config::set( 'cookie', $config );
```

####设置
```
\houdunwang\cookie\Cookie::set('name','houdunren.com',3600,'/','.hdphp.com');
值:houdunwang.com 时间:3600秒 路径：/ 作用域: hdphp.com
```

####获取
```
\houdunwang\cookie\Cookie::get('name');
```

####获取所有
```
\houdunwang\cookie\Cookie::all();
```

####判断
```
\houdunwang\cookie\Cookie::has('name');
```

####删除
```
\houdunwang\cookie\Cookie::del('name');
```

####清空
执行以下代码将删除所有客户端的cookie数据
```
\houdunwang\cookie\Cookie::flush();
```