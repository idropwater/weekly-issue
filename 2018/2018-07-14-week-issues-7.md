# week-6

## GitHub
- dom2image 使用HTML5 canvas从DOM节点生成图像 [dom-to-image](https://github.com/tsayen/dom-to-image)

	```
	// 文件下载
    var link = document.createElement('a');
    link.download = 'my-image-name.jpeg';
    link.href = dataUrl;
    link.click();
	```

- pinyin 汉字拼音 ➜ hàn zì pīn yīn,汉字拼音转换工具。
[pinyin](https://github.com/hotoo/pinyin)


## 学习
- [字符编码笔记：ASCII，Unicode 和 UTF-8
](http://www.ruanyifeng.com/blog/2007/10/ascii_unicode_and_utf-8.html)

- 编码
	- ASCII 是基于拉丁字母的一套计算机编码系统。它主要用于显示现代英语，而其扩展版本EASCII则可以部分支持其他西欧语言[ASCII](https://zh.wikipedia.org/wiki/ASCII)
	
	- Unicode 是计算机科学领域里的一项业界标准。它对世界上大部分的文字系统进行了整理、编码，使得电脑可以用更为简单的方式来呈现和处理文字。[Unicode](https://zh.wikipedia.org/wiki/Unicode)
		- UTF-8 是一种针对Unicode的可变长度字符编码，也是一种前缀码。它可以用来表示Unicode标准中的任何字符，且其编码中的第一个字节仍与ASCII兼容，这使得原来处理ASCII字符的软件无须或只须做少部分修改，即可继续使用[UTF-8](https://zh.wikipedia.org/wiki/UTF-8)

		- UTF-16 本页面包含特殊字符，部分操作系统及浏览器需要特殊字母与符号支持才能正确显示，否则可能出现乱码、问号、空格等其它符号。[UTF-16](https://zh.wikipedia.org/wiki/UTF-16)

		- ...

	- Base64 是一种基于64个可打印字符来表示二进制数据的表示方法。由于 2^{6}=64，所以每6个比特为一个单元，对应某个可打印字符。3个字节有24个比特，对应于4个Base64单元，即3个字节可由4个可打印字符来表示。它可用来作为电子邮件的传输编码。在Base64中的可打印字符包括字母A-Z、a-z、数字0-9，这样共有62个字符，此外两个可打印符号在不同的系统中而不同 [Base64](https://zh.wikipedia.org/wiki/Base64)

- UUID, 通用唯一识别码，是由一组32位数的16进制数字所构成。目的是让分布式系统中的所有元素都能有唯一的辨识信息，而不需要透过中央控制端来做辨识信息的指定。如此一来，每个人都可以创建不与其它人冲突的UUID。在这样的情况下，就不需考虑数据库创建时的名称重复问题。[uuid](https://zh.wikipedia.org/wiki/%E9%80%9A%E7%94%A8%E5%94%AF%E4%B8%80%E8%AF%86%E5%88%AB%E7%A0%81)

- git rebase [Git 分支 - 变基](https://git-scm.com/book/zh/v2/Git-%E5%88%86%E6%94%AF-%E5%8F%98%E5%9F%BA)。

	```
	$ git checkout experiment
	$ git rebase master
	First, rewinding head to replay your work on top of it...
	Applying: added staged command
	
	```
它的原理是首先找到这两个分支（即当前分支 experiment、变基操作的目标基底分支 master）的最近共同祖先 C2，然后对比当前分支相对于该祖先的历次提交，提取相应的修改并存为`临时文件`，然后将当前分支指向目标基底 C3, 最后以此将之前另存为临时文件的修改依序应用。（译注：写明了 commit id，以便理解，下同）

	![alt text](https://git-scm.com/book/en/v2/images/basic-rebase-3.png)

	注意：变基的风险
	呃，奇妙的变基也并非完美无缺，要用它得遵守一条准则：

	不要对在你的仓库外有副本的分支执行变基。

	如果你遵循这条金科玉律，就不会出差错。 否则，人民群众会仇恨你，你的朋友和家人也会嘲笑你，唾弃你。

	变基操作的实质是丢弃一些现有的提交，然后相应地新建一些内容一样但实际上`不同的提交`。 如果你已经将提交推送至某个仓库，而其他人也已经从该仓库拉取提交并进行了后续工作，此时，如果你用 git rebase 命令重新整理了提交并再次推送，你的同伴因此将不得不再次将他们手头的工作与你的提交进行整合，如果接下来你还要拉取并整合他们修改过的提交，事情就会变得一团糟。

	只要你把变基命令当作是在推送前清理提交使之整洁的工具，并且只在从未推送至共用仓库的提交上执行变基命令，就不会有事。 假如在那些已经被推送至共用仓库的提交上执行变基命令，并因此丢弃了一些别人的开发所基于的提交，那你就有大麻烦了，你的同事也会因此鄙视你。