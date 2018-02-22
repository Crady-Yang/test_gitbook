```
# Scp初步
```



    scp指令


    * 上传文件到服务器

    scp【本地文件的路径】【服务器用户名】@【服务器地址】：【服务器上存放文件的路径】
    ```shell
    $ scp /Users/xxx/test/test.sh root@192.168.1.1 /home/deploy

    #输入密码
    $ root@192.168.1.1's password:
    ```
    输入密码后，本地的test.sh文件上传到服务器的某个文件夹下

    * 上传文件夹到服务器
    ```shell
    scp -r /Users/xxx/test root@192.168.1.1:/home/deploy

    #输入密码
    $ root@192.168.1.1's password:
    ```

    * 从服务器下载文件

    scp【服务器用户名】@【服务器地址】：【服务器上存放文件的路径】【本地文件的路径】

    ```shell
    $ scp root@192.168.1.1:/Users/xxx/test/a.sh /home/deploy/test 
    ```

    * 从服务器下载文件夹
    ```shell
    $ scp -r root@192.168.1.1:/Users/xxx/test /home/deploy/test 
    ```


    * scp指令帮助
    ```shell
    $ test scp --help
    scp: illegal option -- -
    usage: scp [-346BCpqrv] [-c cipher] [-F ssh_config] [-i identity_file]
               [-l limit] [-o ssh_option] [-P port] [-S program]
               [[user@]host1:]file1 ... [[user@]host2:]file2
    ```

    OPTIONS：

    -v 和大多数 linux命令中的-v意思一样，用来显示进度。可以用来查看连接、认证、或是配置错误

    -C 使能压缩选项

    -P 选择端口

    -r 复制目录



