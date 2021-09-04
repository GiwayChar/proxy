# 记录一些代理的网址
## git代理的网址
[git代理](https://blog.csdn.net/airlooking/article/details/80168247)
重点是：
```
#只对github.com
git config --global http.https://github.com.proxy socks5://127.0.0.1:1080

#取消代理
git config --global --unset http.https://github.com.proxy
```

## wget代理的网址
[ubuntu 系统代理](https://blog.csdn.net/u011119817/article/details/110856212)
```
重点是：
export proxy_addr=172.18.32.174
export proxy_port=1080

export http_proxy=http://$proxy_addr:$proxy_port
export https_proxy=https://$proxy_addr:$proxy_port
export ftp_proxy=http://$proxy_addr:$proxy_port
export no_proxy=127.0.0.1,localhost

export HTTP_PROXY=http://$proxy_addr:$proxy_port
export HTTPS_PROXY=https///$proxy_addr:$proxy_port
export FTP_PROXY=http://$proxy_addr:$proxy_port
export NO_PROXY=127.0.0.1,localhost
```