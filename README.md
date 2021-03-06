# 一言 API (Hitokoto/ヒトコト)
**重要提示：原 repo 位于 https://github.com/FlyingSky-CN/HitokotoAPI ，而此处 fork 为自用。且如果一下说明未及时更新，则用处很可能与之大相径庭。此外，所使用的数据文件（例如目前可能存在的 hitokoto.txt）不适用从原项目继承的许可，如需使用请单独联系我。**

基于 PHP 的一言 API (Hitokoto/ヒトコト)，非使用数据库（不依赖任何在线API和本地数据库调用一言）。
## 什么是一言
动漫也好、小说也好、网络也好，不论在哪里，我们总会看到有那么一两个句子能穿透你的心。「一言」就好似一个公开的摘抄本，我们在此记录那些让人一眼就有所感触的短句，并通过公共 API 的形式使你能够在自己的项目中调用它们。
## 调用方法
`GET`
## 参数说明
| 参数名  | 类型   | 含义                                    | 默认     |
| ------- | ------ | --------------------------------------- | -------- |
| data    | string | 选择数据来源，可指定为 antwort          | hitokoto |
| charset | string | 返回字符集，支持 utf-8 / gbk            | utf-8    |
| encode  | string | 返回数据格式                            | 空       |
| time    | int    | 值为1时在最后输出运行时间，仅供测试使用 | 空       |
### 数据格式说明
| 参数值 | 含义                                     |
| ------ | ---------------------------------------- |
| json   | 返回 JSON 格式数据                       |
| js     | 返回函数名为 hitokoto 的 JavaScript 脚本 |
| 空     | 返回纯文本                               |
## 响应数据
下面是实际请求一次 index.php?encode=json 的结果：
```
{
"hitokoto":"扎古不论怎么化妆都不可能变成高达的。"
}
```
