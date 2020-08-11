### 使用方式
```
1. 依赖im_lib库，implementation project(':im_lib')
2. 自定义IMSEventListener，实现OnEventListener，重写对应的方法配置参数
3. 自定义IMSConnectStatusListener，实现IMSConnectStatusCallback，重现对应的方法监听ims连接状态
4. 调用IMSClientInterface.init(Vector<String> serverUrlList, OnEventListener listener, IMSConnectStatusCallback callback)方法，把服务器地址列表、IMSEventListener、IMSConnectStatusListener三个参数传入即可。
5. 发送消息：调用IMSClientInterface.sendMsg(MessageProtobuf.Msg msg)即可发送
6. 接收消息：收到消息会回调IMSEventListener.dispatchMsg(MessageProtobuf.Msg msg)方法。
```
