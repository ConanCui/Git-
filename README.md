
# Git使用说明


#### <i class="icon-refresh"></i> 1、git的初始设置


> git config --global user.name "Your Real Name"

> git config --global user.email you@email.address

#### <i class="icon-refresh"></i> 2、建立仓库

> 在git bash里找到你的项目目录。（或直接用shell右键里的git bash here）

> git init

#### <i class="icon-refresh"></i> 3、初始化项目

> git add .

> 留心后面的一个 “.” ， 这是添加所有文件的情况，如果愿意，你也可以添加特定的几个文件，比如git add readme.txt等等。之后就可以做我们的first commit到仓库里了。

> git commit -m 'first commit'

#### <i class="icon-refresh"></i> 4、 注册github账号

> 在github账户上新建repo

#### <i class="icon-refresh"></i> 5、创建SSH密匙

> 这步工作应该是最麻烦的吧。回到桌面，打开git bash，输入以下命令。

> ssh-keygen -C 'your@email.address' -t rsa

> 确认使用默认路径，然后输入两次你要是用的密码就行（一般直接敲几个回车不使用密码）。

#### <i class="icon-refresh"></i> 6、提交密匙

> 现在又要回到github的页面上，在右上方工具栏里找到Account Settings。在这个页面上有一个SSH Public Keys标签，选择Add another public key。Title随便取，Key是一段东西。找到刚才创建密匙的那个目录下（默认是C:\Documents and Settings\你的windows用户名.ssh，OSX是~/.ssh）找到id_rsa.pub文件，把它打开可以看到一堆文字，拷贝下来黏贴到github页面key的空白处。然后Apply，就好了。可以使用以下命令测试连接

> ssh -v git@github.com

> 会要求输入你刚才设置的密码，如果成功的话可以看到这样的ERROR（orz，起码证明连接是成功了）

> ERROR: Hi Arthraim! You've successfully authenticated, but GitHub does not provide shell access
#### <i class="icon-refresh"></i> 7、上传代码

> 最后就是上传你的代码了~ bash切换到你的项目目录下，输入以下命令。

> git remote add origin git@github.com:你的github用户名/你的github项目名.git

> git push origin master


#### <i class="icon-refresh"></i> 8、其他常用命令
> 删除本地git文件夹 rm -rf

