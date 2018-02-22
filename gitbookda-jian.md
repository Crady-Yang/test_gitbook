### mac部分 {#mac部分}

参考链接：[https://www.jianshu.com/p/4824d216ad10](https://www.jianshu.com/p/4824d216ad10)

```
sudo npm install gitbook-cli -g

```

```
一定要用到
-g
，这个代表全局安装，我去掉
-g
安装了一次，也成功了，但是在终端使用
gitbook -V
查看的时候发现根本没安装，这是我遇到的坑最多的地方。
```

```
gitbook -V
CLI version: 2.3.0
GitBook version: 3.2.2

```

安装Gitbook编辑器

下载地址：[https://www.gitbook.com/editor/](https://www.gitbook.com/editor/)

使用步骤

1.新建一本书起名为note1

注意：gitbook地址

```
$
 /Users/xiaoming/GitBook/Library/Import
ote1
```

此时在这个地址生成一个名叫`note1`的文件夹

2.进入自己新建的book文件下

```
$
cd
 /Users/xiaoming/GitBook/Library/Import
ote1
```

3.在该目录下执行`gitbook build`指令

```
➜
  note1 
git:
(master) gitbook build

info:
7
 plugins are installed 

info:
6
 explicitly listed 

info:
 loading plugin 
"highlight"
... OK 

info:
 loading plugin 
"search"
... OK 

info:
 loading plugin 
"lunr"
... OK 

info:
 loading plugin 
"sharing"
... OK 

info:
 loading plugin 
"fontsettings"
... OK 

info:
 loading plugin 
"theme-default"
... OK 

info:
 found 
2
 pages 

info:
 found 
1
 asset files 

info:
>
>
 generation finished with success 
in
0.5
s ! 

```

4.此时note1下生成\_book文件夹

```
➜
  note1 git:(master) ls
README.md   SUMMARY.md  _book       chapter1.md

```

5.执行`gitbook serve`指令

```
➜
  note1 git:(master) gitbook serve
Live reload server started on port: 35729
Press CTRL+C to quit ...

info: 7 plugins are installed 
info: loading plugin "livereload"... OK 
info: loading plugin "highlight"... OK 
info: loading plugin "search"... OK 
info: loading plugin "lunr"... OK 
info: loading plugin "sharing"... OK 
info: loading plugin "fontsettings"... OK 
info: loading plugin "theme-default"... OK 
info: found 2 pages 
info: found 1 asset files 
info: 
>
>
 generation finished with success in 0.6s ! 

Starting server ...
Serving book on http://localhost:4000
^C


```

6.在浏览器输入`http://localhost:4000`就可看到生成的book

### 安装calibre插件 {#安装calibre插件}

calibre是一款非常方便的开源电子书转换软件。

1.calibre官网下载插件，下载链接：[https://calibre-ebook.com/download。下载适合自己系统的版本。](https://calibre-ebook.com/download%E3%80%82%E4%B8%8B%E8%BD%BD%E9%80%82%E5%90%88%E8%87%AA%E5%B7%B1%E7%B3%BB%E7%BB%9F%E7%9A%84%E7%89%88%E6%9C%AC%E3%80%82)

2.执行以下命令

```
sudo ln -s /Applications/calibre.app/Contents/MacOS/ebook-convert /usr/local/bin

```

3.生成pdf文件

```
➜
  note1 git:(master) gitbook pdf . mypdf.pdf
info: 7 plugins are installed 
info: 6 explicitly listed 
info: loading plugin "highlight"... OK 
info: loading plugin "search"... OK 
info: loading plugin "lunr"... OK 
info: loading plugin "sharing"... OK 
info: loading plugin "fontsettings"... OK 
info: loading plugin "theme-default"... OK 
info: found 2 pages 
info: found 1 asset files 
info: 
>
>
 generation finished with success in 8.2s ! 
info: 
>
>
 1 file(s) generated


```

4.进入之前的note1目录，就可以额看到mypdf.pdf文件了

