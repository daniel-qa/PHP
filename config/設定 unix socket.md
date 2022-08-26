php-fpm 的运行端口号和 socket 文件的地址都是在 php-fpm.conf 中配置的。

php-fpm.conf 文件在 php 安装文件的 /etc 目录下，

比如你的 php 安装在 /opt/php 目录，则应该是 /opt/php/php-fpm.conf。

( 也有可能在  /usr/local/etc/ ，但主設定會在 php-fpm.d/ 目錄下)

要打開 unix socket ，要先設定 www.conf
```

listen = 127.0.0.1:9000  # 預設

listen = /var/run/php-fpm.sock
```

php-fpm 的 listen 指令可以通过五种方式处理 FastCGI 请求，分别是：

1. ipv4: 端口号

2. ipv6: 端口号

3. port 相当于 0.0.0.0:port，本机所有 ipv4 对应的端口号

4. [::]:port，包括 ipv4 和 ipv6

5. unix socket 文件


直接配置使用 unix socket 文件之后，会遇到 access deny 的问题，由于 socket 文件本质上还是一个文件，

存在权限控制问题，默认由 root 用户创建，因此 nginx 进程无权限访问，应该配置如下命令：

```

; Set permissions for unix socket, if one is used. In Linux, read/write

; permissions must be set in order to allow connections from a web server. Many

; BSD-derived systems allow connections regardless of permissions.

; Default Values: user and group are set as the running user

; mode is set to 0660

listen.owner = www

listen.group = www

listen.mode = 0660
```
