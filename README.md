# pure

A brand new default theme for [Hexo].

- [Preview](http://blog.cofess.com/)

## 界面

- 主页

![](https://raw.githubusercontent.com/cofess/hexo-theme-pure/dev-gulp/screenshot/home.png)

- 归档

![](https://raw.githubusercontent.com/cofess/hexo-theme-pure/dev-gulp/screenshot/archives.png)

- 分类

![](https://raw.githubusercontent.com/cofess/hexo-theme-pure/dev-gulp/screenshot/categories.png)

## Installation

### Install plugin
hexo-wordcount
```
npm install hexo-wordcount --save
```
hexo-generator-json-content
```
npm install hexo-generator-json-content --save
```
hexo-generator-feed
```
npm install hexo-generator-feed --save
```
hexo-generator-sitemap
```
npm install hexo-generator-sitemap --save
```
hexo-generator-baidu-sitemap
```
npm install hexo-generator-baidu-sitemap --save
```

## Run
```
hexo g
hexo s -w //(-w:watch file change)
```

## Other
### Clean cache
```
hexo-clean
```
### Data files
For example, add links.yml in source/_data folder.

只需我们同样在 hexo 目录下的 source 文件夹内创建一个名为 _data（禁止改名）的文件夹。

然后在文件内创建一个名为 links.yml 的文件,在其中添加相关数据即可。

这里单个友情链接的格式为：
```
Name:
    link: http://example.com
    avatar: http://example.com/avatar.png
    descr: "这是一个描述"
```
添加多个友情链接，我们只需要根据上面的格式重复填写即可。

. 将 Name 改为友情链接的名字，例如 Viosey。

. http://example.com 为友情链接的地址。

. http://example.com/avatar.png 为友情链接的头像。

. 这是一个描述 为友情链接描述。

## 其他插件
### hexo-translate-title
使用Google翻译，百度翻译和有道翻译将Hexo中的汉字标题转成英文标题
https://github.com/cometlj/hexo-translate-title

#### 安装
```bash
npm install hexo-translate-title --save
```
#### 使用
配置hexo根项目下的`_config.yml`

```yml
translate_title:
  translate_way: google    #google | baidu | youdao
  youdao_api_key: XXX
  youdao_keyfrom: XXX
  is_need_proxy: true     #true | false
  proxy_url: http://localhost:8123
```
**注意**：判断是否需要配置google本地代理，因为我在本地是开启时才能访问google翻译的，如果没有被墙，请将`_config.yml` 下的`is_need_proxy: true`改为false。如果设置为true,请设置本地代理地址

#### 翻译效果评估
google翻译 > baidu翻译 > ~~有道翻译~~


### hexo-abbrlink
https://github.com/rozbo/hexo-abbrlink

A [Hexo plugin](https://hexo.io/plugins/) to generate static post link based on post titles.

#### How to install

Add plugin to Hexo:

```
npm install hexo-abbrlink --save
```

Modify permalink in config.yml file:

```
permalink: posts/:abbrlink/
```

There are two settings:

```
alg -- Algorithm (currently support crc16 and crc32, which crc16 is default)
rep -- Represent (the generated link could be presented in hex or dec value)
```

```
#### abbrlink config
abbrlink:
  alg: crc32  #support crc16(default) and crc32
  rep: hex    #support dec(default) and hex
```

#### Sample

The generated link will look like the following:

```
crc16 & hex
https://post.zz173.com/posts/66c8.html

crc16 & dec
https://post.zz173.com/posts/65535.html
```

```
crc32 & hex
https://post.zz173.com/posts/8ddf18fb.html

crc32 & dec
https://post.zz173.com/posts/1690090958.html
```

