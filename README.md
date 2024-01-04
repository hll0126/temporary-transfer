# temporary-transfer
# 当作临时传输的网站使用
# 原因：国内找不到合适的临时传输网站工具，要么就是收费，要么就是文件上传成功在另一台设备却接收失败。
# 方法：
1 首先需要在GitHub上新建一个repository，随后复制库的HTTPS或者SSH，一般是复制HTTPS；

2 其次在本地电脑上的一个文件夹内右键选择Git Bash Here，先初始化git init，后输入git clone url，url是你刚刚复制的HTTPS，此时就会在该位置下载刚刚创建的repository，文件夹名称是你命名repository的名字，记作test；

3 第三，cd到该test文件夹，把你想要传输的文件上复制到该文件夹test下，之后输入git add .或者git add -A，目的是将本地电脑的文件暂时缓存在GitHub上的缓存库中；

4 第四，输入git commit -m "提交信息"，将你刚刚上传在GitHub缓存库中的文件进行信息命名，为的是从GitHub缓存库向GitHub仓库传输进行明确分辨，其中"提交信息"名字不要重复；

5 最后，输入git push，将GitHub缓存库中的文件上传给GitHub仓库中去，可能需要输入你的GitHub账号和密码。

其中，第一步需要首先创建一个GitHub账号，第二步需要安装git软件。

若是只需要下载GitHub上的代码，只需要执行第二步，在电脑的本地位置上，右键Git Bash Here，输入git clone url，url是你需要下载的GitHub代码链接。

若是需要更新GitHub文件库，则在执行第二步后，输入git fetch --all，git reset --hard original/main(或者git reset --hard original/master，需要根据当地代码库的描述来确定)和git pull；
之后在该文件夹下删除文件、增加文件或者替换文件，执行第三步（加入缓存）、第四步（提交信息）和第五步（推入仓库）。

若是需要更新文件，直接git pull就行。
# 参考链接：
1. https://www.cnblogs.com/kumata/p/9061166.html
2. https://zhuanlan.zhihu.com/p/114174753
3. https://zhuanlan.zhihu.com/p/337959303

