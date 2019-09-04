# Blob对象

> 在一般的Web开发中，很少会用到Blob，但Blob可以满足一些场景下的特殊需求。Blob，Binary Large Object的缩写，代表二进制类型的大对象。Blob的概念在一些数据库中有使用到，例如，MYSQL中的BLOB类型就表示二进制数据的容器。在Web中，Blob类型的对象表示不可变的类似文件对象的原始数据，通俗点说，就是Blob对象是二进制数据，但它是类似文件对象的二进制数据，因此可以像操作File对象一样操作Blob对象，实际上，File继承自Blob。

## 创建Blob

可以通过Blob的构造函数创建Blob对象：
`Blob(blobParts[, options])`
参数说明：
`blobParts`： 数组类型， 数组中的每一项连接起来构成Blob对象的数据，数组中的每项元素可以是`ArrayBuffer`(二进制数据缓冲区), `ArrayBufferView`,`Blob`,`DOMString`。或其他类似对象的混合体。
`options`：可选项，字典格式类型，可以指定如下两个属性：

* `type`: 默认值为""，它代表了将会被放入到blob中的数组内容的MIME类型。
* `endings`: 默认值为"transparent"，用于指定包含行结束符\n的字符串如何被写入。 它是以下两个值中的一个： "native"，表示行结束符会被更改为适合宿主操作系统文件系统的换行符； "transparent"，表示会保持blob中保存的结束符不变。
举个栗子：

### 将json对象存储在Blob对象中再存储在FormData中上传文件

```javascript
var jsonObj = { name: 'helloworld' };
var blob = new Blob([JSON.stringify(jsonObj)]);

var formData = new FormData();
formData.append('file', blob);
```

### 分片上传

[参考引用](#引用)

### Blob Url

[参考引用](#引用)

## 引用

详细内容请参考：

[链接 https://www.jianshu.com/p/b322c2d5d778](https://www.jianshu.com/p/b322c2d5d778)
