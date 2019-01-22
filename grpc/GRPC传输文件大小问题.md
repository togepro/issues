###标题
GRPC 传输问题
---
###问题描述
#####ERROR: grpc：received message larger than max(xxxx vs. 4194304)

###有关issue
####[How to set the maximum message size in Python and C#? #15922](https://github.com/grpc/grpc/issues/15922)

###解决办法
#### 在server端代码中，初始化server时添加设置接受信息大小的可选项
```python
server = grpc.server(futures.ThreadPoolExecutor(max_workers=10), 
        options=[(cygrpc.ChannelArgKey.max_send_message_length, -1),
                (cygrpc.ChannelArgKey.max_receive_message_length, -1)])
```