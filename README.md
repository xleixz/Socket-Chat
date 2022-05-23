# Socket聊天室

#### 介绍
基于Java开发的图形化聊天室

#### 使用说明

1.  启动server服务器端
2.  启动client客户端

#### 参与贡献

1.  xleixz@qq.com


#### 实现功能

1.  登录账号：用Java图形界面编写服务器和客户端程序
2.  列表：好友列表显示在客户端上
3.  群聊：可以实现群聊窗口（群聊里所有人的聊天记录均可显示在客户端上）
4.  私聊：可单独给好友发送私聊信息，接收到私聊信息时，自动接收弹出信息消息框
5.  提出去群群聊：服务器端可以强迫指定用户下线
6.  实时显示状态：客户端用户的上线和下线状态可在聊天框中实时显示

### 编写思路

1.  由两部分组成：服务器端和客户端
2.  服务器端可以发送群发信息，管理成员。另外服务器作为一个中转站，客户端发送的信息先由服务器接收，再由服务器端发送给对应的客户端
    服务器端：
        由一个线程来等待客户端的连接，客户端随时可以连接到服务器，服务器端随时接收客户端发送的信息，并每新增一个用户就需要为该用户建立一个聊天的线程
    客户端：
        客户端需要实现的主要功能是群发信息和私发信息，并且通过收刀的信息格式判断服务器发送过来的信息，再进行响应的代码

### 实现效果图
![输入图片说明](https://images.gitee.com/uploads/images/2021/0808/112929_79e14601_8927900.png "QQ图片20210808112909.png")