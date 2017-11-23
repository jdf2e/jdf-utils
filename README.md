[![NPM](https://nodei.co/npm/jdf-utils.png?downloads=true)](https://nodei.co/npm/jdf-utils/)

[![NPM version](https://badge.fury.io/js/jdf-utils.png)](http://badge.fury.io/js/jdf-utils)  [![Build Status](https://travis-ci.org/jdf2e/jdf-utils.svg?branch=master)](https://travis-ci.org/jdf2e/jdf-utils)


# jdf-utils

JDF文件操作和基础函数类库

## Install
```
$ npm install --save jdf-utils
```

## Usage
```
var jdfUtils = require('jdf-utils');
var file = jdfUtils.file;
var base = jdfUtils.base;
```

## file api

判断文件是否存在
```
file.exists(path);
```

判断是否是文件
```
file.isFile(path);
```

判断是否是文件夹
```
file.isDir(path);
```

判断是否是空路径
```
file.isBlankDir(path);
```

判断是否是windows系统
```
file.isWin();
```

获取资源的真实路径
```
file.realpath(path);
```

路径格式化，将`\`替换为`/`
```
file.pathFormat(path);
```

获取当前工作目录
```
file.currentDir();
```

读取文件，默认文件编码为utf-8
```
file.read(path [,encodeing]);
```

写文件，默认文件编码为utf-8
```
file.write(path, source [,encoding]);
```

复制二进制文件
```
file.copyBinary(path, target);
```

删除文件/文件夹
```
file.del(path [,callback]);
```

文件过滤
```
file.filter(path, [include, exclude]);
```

判断文件是否属于以下几种文件类型：`.git`，`.svn`，`Thumbs`，`DS_Store`，`.db`
```
file.excludeFiles(path);
```

文件复制
```
file.copy(path, target, [include, exclude, uncover, move]);
```

`@include`：想要复制的文件后缀，
`@exclude`：不想复制的文件后缀，
`@uncover`：是否不覆盖目标文件，默认为false，
`@move`：想要移动文件，默认为false


下载文件
```
file.download(path, target);
```

创建文件夹
```
file.mkdir(path);
```

读取文件列表
```
file.getdirlist(path);
```

读取JSON文件
```
file.readJSON(path);
```

重命名文件
```
file.renameFile(path);
```

对文件base64编码
```
file.base64Encode(path);
```

## base api

检测是否存在和取widget name
```
base.reg.widget();
```

获取widget type
```
base.reg.widgetType();
```

获取widget data
```
base.reg.widgetData();
```

获取widget 是否有注释
```
base.reg.widgetComment();
```

获取widget position
```
base.reg.widgetPosition();
```

获取当前页面输出的widget name
```
base.reg.widgetOutputName();
```

获取被注释的widget
```
base.reg.commentWidget();
```

获取非注释的widget
```
base.reg.notCommentWidget();
```

匹配link标签
```
base.reg.cssLink();
```

匹配script标签
```
base.reg.jsLink();
```

匹配html注释
```
base.reg.htmlComment();
```
判断是否为数据源文件，默认为json
```
base.is.dataSource(path);
```

判断是否为tpl文件
```
base.istpl(path);
```

判断是否为vm文件
```
base.is.vm(path);
```

判断是否为smarty文件
```
base.is.smarty(path);
```

判断是否为html文件
```
base.is.html(path);
```

判断是否为css文件
```
base.is.css(path);
```

判断是否为less文件
```
base.is.less(path);
```

判断是否为sass文件
```
base.is.sass(path);
```

判断是否为js文件
```
base.is.js(path);
```

判断是否为jpg文件
```
base.is.jpg(path);
```

判断是否为png文件
```
base.is.png(path);
```

判断是否为http链接
```
base.is.httpLink(str);
```

判断是否为图片文件：svg，tiff，wbmp，png，bmp，fax，gif，ico，jfif，jpe，jpeg，jpg，cur，eot，ttf，woff
```
base.is.imageFile(str);
```

判断是否为babel文件
```
base.is.babel(path);
```

去掉path的//
```
base.replaceSlash(path);
```

拼接路径，并替换`\`为`/`
```
base.pathJoin(path);
```

去掉空格
```
base.trim(str);
```

变量存在返回变量,变量不存在返回''
```
base.getVar(str);
```

取当前日期
```
base.getDay();
```

取当前时间
```
base.getTime([separator, hasMs]);
```

`@separator`：分隔符，默认为冒号，
`@hasMs`：是否返回毫秒数

获取时间戳
```
base.getTimestamp();
```

判断是否为数组
```
base.isArray(obj);
```

获取css文件扩展名
```
base.getCssExtname(path);
```

获取js文件扩展名
```
base.getJsExtname(path);
```

获取url的参数
```
base.getUrlParam(url);
```

发起http请求
```
base.httpget(url);
```

数组去重
```
base.uniq(array);
```

对象合并
```
base.merageObj(obj1, obj2);
```

判断`array`是否包含`str`
```
base.inArray(array, str);
```

返回字符串的md5值
```
base.md5(str);
```

获取当前电脑用户信息
* `username`，当前用户电脑帐户名称
* `node_path`，当前电脑上的 nodejs 全局安装包位置
* `pwd`，当前用户执行的项目路径
```
base.getUserInfo();
```
















