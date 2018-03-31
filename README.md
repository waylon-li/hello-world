# hello-world

### github 的使用：

##### 1、连接本机和网络仓库，使用git获取SSH密钥在github 中添加SSH；

	git_bash:	ssh-keygen -t rsa -C "myemil@myemail.com"

##### 2、检查是否配置成功，yes后返回success信息；
	git_bash:	ssh -T git@github.com

##### 3、配置git的个人信息；
	git_bash:	git config --global user.name "waylon_li"
	git_bash:	git config --global user.email 	"myemail@myemail.com"

##### 4、在guthub 上建立版本仓库，在git 中clone 该仓库；
	git_bash:	git clone https//github.com/waylon-li/hello-worls.git

##### 5、在本机修改版本，用git commit 进行提交到本机的版本中；
	git_bash:	git add README.md
	git_bash:	git commit -m "github 的使用;"

##### 6、提交到guthub 的网络版本库中；
	git_bash:	git push origin master
