# week-6

## GitHub
- 一个漂亮的提示信息的库 [sweetalert](https://sweetalert.js.org/guides/)

- 提供了百度坐标（BD09）、国测局坐标（火星坐标，GCJ02）、和WGS84坐标系之间的转换 [coordtransform](https://github.com/wandergis/coordtransform)

- GeoJSON的解释器和序列化器 [wkx](https://github.com/cschwarz/wkx)

- 基于LZ的JavaScript压缩算法 [lz-string](https://github.com/pieroxy/lz-string)

- 一步一步地介绍网站和功能 [intro-guide-js](https://github.com/johanlahti/intro-guide-js#readme), [intro.js](https://github.com/usablica/intro.js)

- md5算法实现 [spark-md5](https://github.com/satazor/js-spark-md5#readme)

- [core-decorators](https://github.com/jayphelps/core-decorators)

## 教程
- 前端自动化测试 
	- [cypress API](https://example.cypress.io/) 以及 [cypress 文档](https://docs.cypress.io/guides/overview/why-cypress.html#)

	- [page-object](https://github.com/cheezy/page-object)

	- [测试驱动开发TDD](https://zh.wikipedia.org/wiki/%E6%B5%8B%E8%AF%95%E9%A9%B1%E5%8A%A8%E5%BC%80%E5%8F%91)

	- [行为驱动开发BDD](https://zh.wikipedia.org/wiki/%E8%A1%8C%E4%B8%BA%E9%A9%B1%E5%8A%A8%E5%BC%80%E5%8F%91)


## 学习
- [数据压缩wiki](https://zh.wikipedia.org/wiki/%E6%95%B0%E6%8D%AE%E5%8E%8B%E7%BC%A9) 数据压缩或者源编码是按照特定的编码机制用比未经编码少的数据比特（或者其它信息相关的单位）表示信息的过程。例如，如果我们将“compression”编码为“comp”那么这篇文章可以用较少的数据位表示。常见的例子是ZIP文件格式，此格式不仅仅提供压缩功能，还可作为归档工具（Archiver），能够将许多文件存储到同一个文件中。

- [MD5消息摘要算法](https://zh.wikipedia.org/wiki/MD5)
	- （英语：MD5 Message-Digest Algorithm），一种被广泛使用的密码散列函数，可以产生出一个128位（16字节）的散列值（hash value），用于确保信息传输完整一致。
	- MD5已经广泛使用在为文件传输提供一定的可靠性方面。例如，服务器预先提供一个MD5校验和，用户下载完文件以后，用MD5算法计算下载文件的MD5校验和，然后通过检查这两个校验和是否一致，就能判断下载的文件是否出错。

- [Drag and Drop API](https://developer.mozilla.org/en-US/docs/Web/API/HTML_Drag_and_Drop_API)
	- 可拖拽元素，属性必须draggable为true，ondragstart
	- 目标元素，为drop的区域，ondrop，ondragover
	- 通过event的dataTransfer对象传递数据或者图像等，dataTransfer对象有setData, getData等方法，以及files(拖拽的文件)、dropEffect等属性

- F[File API](https://developer.mozilla.org/zh-CN/docs/Web/API/File)
	- `<input>` 元素上选择文件后返回的 FileList 对象
	- 自由拖放操作生成的 DataTransfer 对象  
	- new File(bits, name[, options])

- [阮老师的教程ArrayBuffer](http://es6.ruanyifeng.com/#docs/arraybuffer)
	- 用来表示通用的、固定长度的原始二进制数据缓冲区。ArrayBuffer 不能直接操作，而是要通过类型数组对象或 DataView 对象来操作，它们会将缓冲区中的数据表示为特定的格式，并通过这些格式来读写缓冲区的内容。

	```
	创建了一个 8 字节的缓冲区 new ArrayBuffer(8)
	```
- [Blob API](https://developer.mozilla.org/zh-CN/docs/Web/API/Blob)
	- 对象表示一个不可变、原始数据的类文件对象。Blob 表示的不一定是JavaScript原生格式的数据。File 接口基于Blob，继承了 blob 的功能并将其扩展使其支持用户系统上的文件。
	
	```
	var aFileParts = ['<a id="a"><b id="b">hey!</b></a>']; // 一个包含DOMString的数组
	var oMyBlob = new Blob(aFileParts, {type : 'text/html'}); // 得到 blob
	```

- [Base64 wiki](https://en.wikipedia.org/wiki/Base64)是一组相似的二进制到文本(binary-to-text)的编码规则，使得二进制数据在解释成radix-64的表现形式后能够用ASCII字符串的格式表示出来。Base64 这个词出自一种MIME数据传输编码。

- [FormData API](https://developer.mozilla.org/zh-CN/docs/Web/API/FormData/Using_FormData_Objects) FormData对象用以将数据编译成键值对，以便用XMLHttpRequest来发送数据。其主要用于发送表单数据，但亦可用于发送带键数据(keyed data)，而独立于表单使用。如果表单enctype属性设为multipart/form-data ，则会使用表单的submit()方法来发送数据，从而，发送数据具有同样形式。
```
var formData = new FormData();formData.append("username", "Groucho");
```








