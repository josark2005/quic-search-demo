# quic-search-demo

Demo for Quic Search

## 白名单（必须）

设置`whitelist.txt`

```txt
# QCS Login Whitelist
# 一行一个授权码
quicdemo
quicdemo2
```

**注意： 授权码并不是安全保障，授权码可以多次登录，且无后台验证机制**

## 数据库列表

设置`lists.txt`

```txt
# 数据库列表
# 名称,文件名,状态（0不可见，1正常，2维护）
# 数据库文件保存在databases文件夹内

不可见示例数据库,test,0
示例数据库,test,1
维护示例数据库,test,2
```

## 增加数据库

新建一个数据库文件，这里以`demo.qcsd`为例

- 使用`文本编辑器（或记事本）`打开`demo.qcsd`
- 按以下格式填充数据库

```txt
# NAME = 数据库名称
# VERSION = v1.0

-> 搜索值（题目）
=> 返回值（答案）
```

- 保存至`./databases/demo.qcsd`
- 在数据库列表中新增这个数据库，如：

```txt
示例数据库,demo,1
```

## 百度翻译支持

设置`config.json`

```json
{
  "TSLTAPI_APPID": "BAIDU_TRANSLATE_APPID",
  "TSLTAPI_KEY": "BAIDU_TRANSLATE_KEY"
}
```

`BAIDU_TRANSLATE_APPID`替换为`百度翻译API`的`APPID`

`BAIDU_TRANSLATE_KEY`替换为`百度翻译API`的`KEY`
