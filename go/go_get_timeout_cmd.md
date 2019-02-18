###go get 安装库超时问题

---
###问题描述
    由于一些go库的安装需要翻墙，或者安装库的时候会执行Fetching go get ...一些墙外库的问题。
    
    这时即使机器已经能够访问外网，但是Windows下的cmd依旧无法访问外网，这就造成go get 超时的问题。

    

###有关链接
- [为Windows cmd设置代理](https://blog.csdn.net/lovelyelfpop/article/details/69586366)
- [golang安装grpc](https://blog.csdn.net/cjj198561/article/details/78133193)


###解决办法

- 第一种情况：直接安装库的情况，这时可不用访问外网安装，GitHub上会有相应的库可使用，go clone 到gopath中，执行go install 相应库即可。 
- 第二种情况：安装库的过程中获取墙外库，这时在本机可访问外网的情况下，为cmd设置临时代理即可使用go get 安装一些墙外库。