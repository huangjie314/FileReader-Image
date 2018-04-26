# FileReader & Image

> 前端完成文件类型上传

> 这里主要使用到H5的FileReader对象来完成。FileReader 对象允许Web应用程序异步读取存储在用户计算机上的文件（或原始数据缓冲区）的内容，使用 File 或 Blob 对象指定要读取的文件或数据。

#### FileReader()
> 返回一个新构造的FileReader。

### FileReader接口的方法：

```
readAsBinaryString            file                       将文件读取为二进制编码
readAsText                    file,[encoding]            将文件读取为文本，其中第二个参数是文本的编码方式，默认值为 UTF-8
readAsDataURL                 file                       将文件读取为DataURL
abort                         (none)                     中断读取操作(无论读取成功或失败，方法并不会返回读取结果，这一结果存储在result属性中)
```


### 相关事件：


```
onabort                               中断
onerror                               出错
onloadstart                     　    开始
onprogress                            正在读取
onload                                成功读取
onloadend                             读取完成，无论成功失败
```

> 文件一旦开始读取，无论成功或失败，实例的 result 属性都会被填充。如果读取失败，则 result 的值为 null ，否则即是读取的结果。

> 如果读取文件过大的话fileReader允许分段读取文件；

---
### base64编码的优缺点：
优点：

1. 减少了http请求。
2. 没有跨域的问题。
3. 直接放在路径里不需要清理缓存。

缺点：
1. IE6/7不支持(不过这个问题不大)；
2. base64本质上是将图片以二进制的字母展示，字符量过大无形中增加了css/html文件的大小；

