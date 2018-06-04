# week issues 2

## 工具
  1. node版本管理工具 [nvm](https://github.com/creationix/nvm)

  2. node 进程管理管理工具 [pm2](http://pm2.keymetrics.io/)

  3. 使用vue复用h5跟小程序代码 [mpvue](https://github.com/mpvue)   

## 教程
  1. 如何搭建git服务器？
    * 服务端安装git并运行git服务，创建git用户
    * 客户端ssh-keygen生成公钥并拷贝至服务器/home/git/.ssh/authorized_keys
    * 服务端初始化git裸仓，并将所有者改为创建的git用户
    * 出于安全考虑，禁止git用户登录shell (将git用户的bash改为git-shell)
    * 客户端克隆远程仓库 git clone git@server:/sample/sample.git, 使用绝对地址，即以根目录/home开始

  2. 如何部署nodejs应用？
    * 服务端需要用到的工具 nvm node版本管理以及pm2 node 进程管理工具
    * 应用程序app.js createServer 并监听端口，安全组必须添加开放该端口的访问
    * 一切正常，客户端即可通过服务端 IP + port 访问

  3. SFTP ssh文件传输协议
    * sftp [user@]host[:file ...] 登录
    * get/put [filename] 从远程下载/上传文件到本地
    * get/put -r [folder] 从远程下载／上传文件包到本地
    * pwd、ls、mkdir、rename、rm、bye、touch、mkdir、 chmod...

## Github
  1. [build your own x](https://github.com/danistefanovic/build-your-own-x) 学习某一项技术的时候最好的方式就是试着将它实现出来

  2. [Ramda](https://ramdajs.com/) 一个javascript函数库。俗话说得好有了锥子，看什么都是钉子

  3. [javascript-algorithms](https://github.com/trekhleb/javascript-algorithms) 是时候研读一下了

## 金句
  1. I’m a firm believer in the idea that the best way to learn a technology is to build it

## 读书
  [算法导论](https://github.com/threerocks/studyFiles/blob/master/%E5%90%8E%E7%AB%AF/%E7%AE%97%E6%B3%95%E5%AF%BC%E8%AE%BA.pdf)


  1. 树
    * 一般树的实现 firstChild + nextSibling
    * 二叉树的实现 leftChild + rightChild

  2. 表达式树: 
    * 如何构建表达式树：后缀表达式 + 栈，类似后缀求值法
    * 前序遍历：前缀表达式
    * 中序遍历
    * 后序遍历：后缀表达式？

  3. 二叉查找树 BST
    * 定义 根节点大于左子树所有值，小于由子树所有值
    * 特性 中序遍历下是有序的，最大值在右下角，最小值在左下角
    * ADT实现 makeEmpty、find、findMin、findMax、insert 、delete !！、retrieve
    * delete 1）只有左子树 2）只有右子树 3）有左子树和右子树（由后继替换） 

  3. 平衡二叉树 AVL
    * 定义 左右子树的高度最多相差1，查询logN的时间复杂度
    * 节点引入平衡因子，0等高，1左高，-1右高
    * 插入四种情况：左儿子左子树（单旋）、左儿子柚子树（双旋）、右儿子左子树（双旋）、右儿子右子树（单旋）
    * 插入元素 ： 1. 左高右低，衡因子符号相同， 右旋 2. 右高左低， 衡因子符号相同，左旋 3. 左高右低，衡因子符号不同， 右旋先左旋再右旋 4. 右边高，左边低，衡因子符号不同，需要先右旋再左旋