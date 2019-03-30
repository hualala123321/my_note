
## sass
+ 安装环境  ruby https://rubyinstaller.org/downloads/   WITHOUT DEVKIT
+ 安装 记得勾选Add Ruby executables to your PATH
+ 成功之后黑窗口 测试 ruby -v
+ 替换源(gem是ruby的包管理工具,因为自带的源国内无法使用,所以需要替换为国内的镜像源)
	- gem sources --remove https://rubygems.org/
	- gem sources -a https://gems.ruby-china.com    修改过可用的源
	- gem sources -l   是否成功
	- gem install sass   gem install compass
	- sass -v  验证sass安装是否成功


### 编译sass
在项目文件里黑窗口。
+ 命令行编译
- 单文件转换命令
```
	sass input.scss output.css
```
- 单文件监听命令
```
	sass --watch input.scss:output.css
```
- 如果你有很多的sass文件的目录，你也可以告诉sass监听整个目录：
```
	sass --watch app/sass:public/stylesheets
```