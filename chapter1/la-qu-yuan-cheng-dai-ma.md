### 拉取远程代码

在本地代码库clone远程代码

> ~ git clone [http://192.168.2.135:8082/xxxx/xxxx.git](http://192.168.2.135:8082/xxxx/xxxx.git)

至此本地文件系统有了本系统代码

## 说明

1. 获得的代码默认是git的`master`分支
2. 开发者对master分支**无权限**`push`
3. 开发时，还请自建新分支，避免本地`master`分支提交（push）至远程代码仓库的`其他分支`，造成`head`混乱



