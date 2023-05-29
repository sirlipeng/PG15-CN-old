# PG15-CN

# PostgreSQL15中文手册翻译计划   
PostgreSQL官方手册是PostgreSQL非常重要的学习和参考资料。本项目进行PostgreSQL15手册的中文化。

## 文档翻译组

本项目得到了山东大学的大力支持。

## Github托管仓库
https://github.com/sirlipeng/PG15-CN

本Github仓库存放已翻译好的sgml文件，通过这些sgml文件可编译成html和pdf等各种格式的文档。
本Github仓库接受对已翻译好的文档的质量改善，欢迎读者的反馈和修正（通过Issues和Pull requests）。

## 翻译管理
https://github.com/sirlipeng/PG15-CN/wiki

## 文档的编译

PG 10以后的文档编译需要在Linux/UNIX上执行

以下说明以10.1为例

  1 . 下载本Github仓库
```shell
git clone https://github.com/postgres-cn/pgdoc-cn.git
```

  2 . 下载对应版本的PostgreSQL源码并解压
```shell
wget https://ftp.postgresql.org/pub/source/v10.1/postgresql-10.1.tar.gz
tar xzf postgresql-10.1.tar.gz
```

  3 . 拷贝github中的sgml文件到PostgreSQL源码中的
```shell
cp -rf pgdoc-cn/postgresql/doc/src/sgml postgresql-10.1/doc/src/
```

  5 . 下载编译PG手册所必需的工具集

参考：http://www.postgresql.org/docs/10/static/docguide-toolsets.html

比如，在RHEL/CentOS上需要安装以下软件，注意docbook-style-xsl的版本必须是1.77.0以上。

	yum install docbook-dtds docbook-style-xsl fop libxslt opensp


  6 .  编译PG手册
```shell
cd postgresql-10.1/
./configure
cd doc/src/sgml
make html
```
参考：http://www.postgresql.org/docs/10/static/docguide-build.html

  7 . 查看编译效果
打开以下html查看编译效果

postgresql-10.1/doc/src/sgml/html/index.html

## 编译生成PDF等格式的离线文档

参考[PostgreSQL离线手册发布步骤](https://github.com/postgres-cn/pgdoc-cn/wiki/PostgreSQL离线手册发布步骤) 生成PDF等格式的离线文档


## 其它
1. Github仓库中的sgml文件编码是UTF8。




