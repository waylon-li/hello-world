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


### linux下github 的使用：

##### 1、centos 下默认开启了SSH，使用 ls -al ~/.ssh 命令查看ssh key是否存在，如存在忽略该步骤；
	生成SSH KEY：ssh-keygen -t rsa -C "myemail@myemail.com"
	生成过程中会让填写passphrase，连按三次回车跳过即可

##### 查看SSH KEY；
	进入～/.ssh 目录，查看id_rsa 和id_rsa_pub 文件
	id_rsa为私钥，id_rsa.pub 为公钥

##### 复制SSH KEY； 
	打开id_rsa.pub 文件，将内容复制到粘贴板
	SSH KEY 公钥用于GitHub 身份验证

##### 添加SSH KEY
	登录GitHub，打开Personal settings 页面，选择SSH and GPG keys 选项
	New SSH key，把复制的内容粘贴到key下
	添加SSH key后，Linux就可以通过SSH 建立本地Git 与GitHub 的连接了

##### 在GitHub 中创建一个仓库，将其clone 到本地
	第一次连接需要确认GitHub 的key 的指纹信息是否真的来自GitHub 的服务器
	克隆到本地的仓库会自动关联远程仓库，可以通过git remote -v 命令查看关联状态
	关联通过后可以通过 git push origin master 命令推送修改

	git add README.md
	git commit -m "add linux info"
	git push origin master

^_^ success!
