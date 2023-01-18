# xWenChen.github.io
WenChen的个人博客存储地址

博客访问地址：https://xwenchen.github.io/

hexo 分支备份了环境文件，是博客内容与配置分支
master 分支存放静态文件，是博客编译内容的存放分支

每次发布新文章或修改网站样式文件时，git add . & git commit -m "some description" & git push origin hexo
	即可把环境文件推送到hexo分支。
	
然后再hexo g -d(或者输入 hexo clean & hexo g & hexo d 指令)发布网站并推送静态文件到master分支。

--------------------------------------------------------------------------------------------------------------

hexo 在新电脑下的环境搭建

新电脑中的环境搭建
这部分应该要简单一点，如果你已经搭建过一个hexo博客的话。

1、新电脑上安装node.js (建议 12 版本，高版本会出错)和git。不赘述。

2、安装hexo：npm install -g hexo-cli。

3、clone远程仓库到本地 git clone https://github.com/xWenChen/xWenChen.github.io.git

4、根据packge.json安装依赖npm install。

5、最后安装部署插件：npm install hexo-deployer-git --save

6、本地生成网站并开启博客服务器：hexo g & hexo s。

7、如果一切正常，此时打开浏览器输入http://localhost:4000/已经可以看到博客正常运行了。

注意：

1、在新电脑上，得预先添加ssh key（具体百度）

2、新电脑中博客不显示内容，是因为主题文件夹为空，需要在提交hexo分支环境之前就把其中.git .gitignore 删除掉。
	或者是git rm -r --cached next，取消对next之前的追踪记录。
