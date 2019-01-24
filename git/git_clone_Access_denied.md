###标题
Git clone error
---
###问题描述
Remote： HTTP Basic : Access denied
fatal :Authentication failed for "http:...."
<center>
![错误信息](../iamges/git_clone_err.jpg)
</center>

###有关链接
- [Git Access denied](https://blog.csdn.net/xiatianyangwang/article/details/78652313)
- [HTTP Basic: Access denied fatal: Authentication failed
](https://stackoverflow.com/questions/44514728/http-basic-access-denied-fatal-authentication-failed)

###解决办法
因为重置了密码导致git远程操作失败，所以使用管理员打开终端，输入命令：

<center>`git config --system --unset credential.helper`</center>