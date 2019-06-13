# 项目说明:
## 数据库设计:  
* 用户表:user(id, uid, name, password)  
* 用户好友关系表:relations(id, uid1, uid2, deleted)  
* 在线用户表:online(id, uid)  
* 用户发送消息表:message(id, uid1, uid2, message)
## 服务器功能:
* 登录
* 注册
* 添加好友
* 删除好友
* 获取好友列表(在线/离线)
* 处理发送消息
## 客户端功能:
pass
## 数据结构:
* 消息:采用结构体  
```
struct msg{     //定义消息
    int type;       //消息类型:0.注册消息MSG_REG, 1.登录消息MSG_LOGIN, 2.退出消息MSG_EXIT, 3.一对一聊天MSG_CHAT
    int senderid;       //发送者id
    int recverid;       //接受者id
    char content[1012];     //消息正文
};
```
