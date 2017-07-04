* handler在初始化时就会执行，而childHandler会在客户端成功connect后才执行，这是两者的区别。

MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=0, _data={"device_id":"49E34C022874CB035EFB2052674DAFA9","platform":3,"uid":"10133","company_id":10034,"php_version":"v1.6.0","sig":"a524ff8ae0c9e6d59ec33e59b96b069ebb83b0e7","state":4},resentCount=0]

{accountProcessor=com.shaozi.im.processors.AccountProcessor@2e6d602f, heartbeatProcessor=com.shaozi.im.protocol.processor.HeartBeatProcessor@24a6f3d7, chatGroupProcessor=com.shaozi.im.processors.ChatGroupProcessor@195304a4, messageProcessor=com.shaozi.im.processors.MessageProcessor@7041ebab, profileProcessor=com.shaozi.im.processors.ProfileProcessor@35689194, oaProcessor=com.shaozi.im.processors.OAProcessor@2643e4a5, closeableProcessor=com.shaozi.im.protocol.processor.CloseableProcessor@2734b2ed}

{1=[com.shaozi.im.processors.AccountProcessor@7355f3d3], 2=[com.shaozi.im.processors.OAProcessor@665c6b18], 3=[com.shaozi.im.processors.ProfileProcessor@5dfb34], 101=[com.shaozi.im.protocol.processor.CloseableProcessor@5c4a5b87], 6=[com.shaozi.im.processors.MessageProcessor@73d33c71], 9=[com.shaozi.im.protocol.processor.HeartBeatProcessor@76528db8], 11=[com.shaozi.im.processors.ChatGroupProcessor@19395c1d]}

public com.shaozi.im.protocol.core.StatusImResult com.shaozi.im.processors.AccountProcessor.doLogin(com.shaozi.im.protocol.processor.base.ProcessorRequest,com.shaozi.im.lib.data.bean.CheckSigBean) throws com.shaozi.lib.throwable.SzException

MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=0, _data={"code":0,"key":"de0fac613357e8a59341bad530becdaf","onlineState":{"status":4,"mStatus":0,"webStatus":0,"uid":"10133"}},resentCount=0]

MessagePack [_flag=1, _code=2, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=0, _data={"status":4,"mStatus":0,"webStatus":0,"uid":"10133"},resentCount=0]

MessagePack [_flag=1, _code=4, _messageId=0,reserved=0, _version=0, _statusCode=0, ack=0, _data={"connClosed":true,"isExceptionCause":false},resentCount=0]

* http://www.blue-zero.com/WebSocket/
 [http://blog.csdn.net/danteliujie/article/details/52458518](http://blog.csdn.net/danteliujie/article/details/52458518)



 MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
 MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=0, _data={"code":0,"key":"32a01ca5f198abff77c98ca74ebc1618","onlineState":{"status":4,"mStatus":0,"webStatus":0,"uid":"10086"}},resentCount=0]
 MessagePack [_flag=1, _code=7, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
 MessagePack [_flag=1, _code=7, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
 MessagePack [_flag=1, _code=7, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=0, _data={"10086":{"status":4,"mStatus":0,"webStatus":0,"uid":"10086"}},resentCount=0]
 MessagePack [_flag=11, _code=2, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
 MessagePack [_flag=6, _code=18, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
 MessagePack [_flag=6, _code=17, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
 MessagePack [_flag=11, _code=2, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=0, _data={"insert":[],"update":[],"delete":[],"maxIdentity":1496137474221},resentCount=0]
 MessagePack [_flag=6, _code=18, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=0, _data=[{"to":"24","count":0}],resentCount=0]
 MessagePack [_flag=6, _code=17, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[],"revokes":[],"datas":[],"updateId":1497358309497},resentCount=0]
 MessagePack [_flag=1, _code=7, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=0, _data={"10086":{"status":4,"mStatus":0,"webStatus":0,"uid":"10086"}},resentCount=1]
 MessagePack [_flag=3, _code=2, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
 MessagePack [_flag=3, _code=2, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":0},resentCount=0]


 2017-06-13 22:18:24,340 (OutPackExecutor.java:72) INFO  com.shaozi.im.protocol.out.OutPackExecutor - sock fail:OutContianerItemBean [ctx=ChannelHandlerContext(ProcessCenterHandler#0, [id: 0xdd068f5d, L:/127.0.0.1:1133 ! R:/127.0.0.1:64309]), pack=MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=0, _data={"code":0,"key":"8175136a5e5bc11858fde50ca3f22f77","onlineState":{"status":4,"mStatus":0,"webStatus":0,"uid":"10086"}},resentCount=0]]
2017-06-13 22:18:25,123 (OutPackExecutor.java:72) INFO  com.shaozi.im.protocol.out.OutPackExecutor - sock fail:OutContianerItemBean [ctx=ChannelHandlerContext(ProcessCenterHandler#0, [id: 0x85290bef, L:/127.0.0.1:1133 ! R:/127.0.0.1:64057]), pack=MessagePack [_flag=9, _code=1, _messageId=8,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]]
2017-06-13 22:18:25,816 (OutPackExecutor.java:72) INFO  com.shaozi.im.protocol.out.OutPackExecutor - sock fail:OutContianerItemBean [ctx=ChannelHandlerContext(ProcessCenterHandler#0, [id: 0x85290bef, L:/127.0.0.1:1133 ! R:/127.0.0.1:64057]), pack=MessagePack [_flag=9, _code=1, _messageId=9,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]]
2017-06-13 22:18:26,529 (OutPackExecutor.java:72) INFO  com.shaozi.im.protocol.out.OutPackExecutor - sock fail:OutContianerItemBean [ctx=ChannelHandlerContext(ProcessCenterHandler#0, [id: 0x85290bef, L:/127.0.0.1:1133 ! R:/127.0.0.1:64057]), pack=MessagePack [_flag=9, _code=1, _messageId=10,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]]
2017-06-13 22:18:27,231 (OutPackExecutor.java:72) INFO  com.shaozi.im.protocol.out.OutPackExecutor - sock fail:OutContianerItemBean [ctx=ChannelHandlerContext(ProcessCenterHandler#0, [id: 0x85290bef, L:/127.0.0.1:1133 ! R:/127.0.0.1:64057]), pack=MessagePack [_flag=9, _code=1, _messageId=11,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]]

*apk反编译 c:/apk-unpack
 http://blog.csdn.net/dreamer2020/article/details/52761606

设备1

----pack in---:MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=0, _data={"device_id":"49E34C022874CB035EFB2052674DAFA9","platform":3,"uid":"99","company_id":10002,"php_version":"v1.6.0","sig":"bbd781af9d8bf797cd69659e0fa833f01e4834ea","state":4},resentCount=0]
2017-06-20 15:27:12,661 (BaseRPC.java:32) INFO  com.shaozi.data.rpc.base.BaseRPC - sz-versionv1.6.0,url:http://dev.t.u.shaozi.com/Server/Auth
----pack out---:MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
2017-06-20 15:27:14,611 (AccountProcessorAdapter.java:244) WARN  com.shaozi.im.business.adapter.processor.AccountProcessorAdapter - rpc request(check):2015(ms)
----pack out---:MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=0, _data={"code":0,"key":"8e99ea31daf876762525ab0822b92e06","onlineState":{"status":4,"mStatus":0,"webStatus":0,"uid":"99"}},resentCount=0]
----pack in---:MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

----pack in---:MessagePack [_flag=1, _code=7, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=1, _code=7, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

----pack out---:MessagePack [_flag=1, _code=7, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=0, _data={"99":{"status":4,"mStatus":0,"webStatus":0,"uid":"99"}},resentCount=0]


----pack in---:MessagePack [_flag=11, _code=2, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":1496824323778},resentCount=0]
----pack in---:MessagePack [_flag=1, _code=7, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=11, _code=2, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

----pack in---:MessagePack [_flag=6, _code=18, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=0, _data={"tos":["24"]},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=18, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

----pack in---:MessagePack [_flag=6, _code=17, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":1497932861969},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=17, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

六月 20, 2017 3:27:15 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:3, serverValue:30}] to 127.0.0.1:27017
六月 20, 2017 3:27:15 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:4, serverValue:31}] to 127.0.0.1:27017
2017-06-20 15:27:15,377 (ProcessHandlerManagerAOP.java:50) WARN  com.shaozi.im.aop.ProcessHandlerManagerAOP - flag:6,code:18,runs(ms):636--ChannelHandlerContext(ProcessCenterHandler#0, [id: 0x4c2e6be6, L:/10.3.21.117:1122 - R:/10.3.21.117:54407])
2017-06-20 15:27:15,380 (ProcessCenter.java:139) INFO  com.shaozi.im.protocol.processor.ProcessCenter - exec(ms):639;msgpack=MessagePack [_flag=6, _code=18, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=0, _data={"tos":["24"]},resentCount=0]

----pack out---:MessagePack [_flag=6, _code=18, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=0, _data=[{"to":"24","count":0}],resentCount=0]

----pack in---:MessagePack [_flag=6, _code=18, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

----pack out---:MessagePack [_flag=6, _code=17, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[],"revokes":[],"datas":[],"updateId":1497932861969},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=17, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


2017-06-20 15:27:15,660 (ProcessHandlerManagerAOP.java:50) WARN  com.shaozi.im.aop.ProcessHandlerManagerAOP - flag:11,code:2,runs(ms):969--ChannelHandlerContext(ProcessCenterHandler#0, [id: 0x4c2e6be6, L:/10.3.21.117:1122 - R:/10.3.21.117:54407])
2017-06-20 15:27:15,662 (ProcessCenter.java:139) INFO  com.shaozi.im.protocol.processor.ProcessCenter - exec(ms):971;msgpack=MessagePack [_flag=11, _code=2, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":1496824323778},resentCount=0]
----pack out---:MessagePack [_flag=11, _code=2, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=0, _data={"insert":[],"update":[],"delete":[],"maxIdentity":1496824323778},resentCount=0]
----pack in---:MessagePack [_flag=11, _code=2, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

----pack in---:MessagePack [_flag=3, _code=2, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":0},resentCount=0]
----pack out---:MessagePack [_flag=3, _code=2, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=3, _code=2, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":0},resentCount=0]
----pack in---:MessagePack [_flag=3, _code=2, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


设备2
----pack in---:MessagePack [_flag=9, _code=1, _messageId=443,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=1, _code=1, _messageId=444,reserved=0, _version=0, _statusCode=0, ack=0, _data={"company_id":"10002","device_id":"A100005C51F04B","php_version":"v1.6.0","platform":"4","sig":"826449c7cdf837370d8b976fb29182ad8e2d9909","state":4,"uid":"100"},resentCount=0]
六月 20, 2017 4:48:34 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:22, serverValue:57}] to 127.0.0.1:27017
2017-06-20 16:48:34,275 (BaseRPC.java:32) INFO  com.shaozi.data.rpc.base.BaseRPC - sz-versionv1.6.0,url:http://dev.t.u.shaozi.com/Server/Auth
----pack out---:MessagePack [_flag=9, _code=1, _messageId=443,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=1, _code=1, _messageId=444,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=9, _code=1, _messageId=30,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=9, _code=1, _messageId=30,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
2017-06-20 16:48:36,287 (AccountProcessorAdapter.java:244) WARN  com.shaozi.im.business.adapter.processor.AccountProcessorAdapter - rpc request(check):2015(ms)
----pack out---:MessagePack [_flag=1, _code=2, _messageId=7,reserved=0, _version=0, _statusCode=0, ack=0, _data={"status":0,"mStatus":4,"webStatus":0,"uid":"100"},resentCount=0]
----pack out---:MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=0, _data={"code":0,"key":"b724a025dc26735e741e2dd5ea14c91b","onlineState":{"status":0,"mStatus":4,"webStatus":0,"uid":"100"}},resentCount=0]
----pack in---:MessagePack [_flag=1, _code=2, _messageId=7,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=11, _code=2, _messageId=445,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":1496824323778},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=17, _messageId=446,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":1497925161529},resentCount=0]
----pack out---:MessagePack [_flag=11, _code=2, _messageId=445,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=6, _code=18, _messageId=447,reserved=0, _version=0, _statusCode=0, ack=0, _data={"tos":["24"]},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=17, _messageId=446,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=3, _code=2, _messageId=448,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":0},resentCount=0]
六月 20, 2017 4:48:36 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:23, serverValue:58}] to 127.0.0.1:27017
六月 20, 2017 4:48:36 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:24, serverValue:59}] to 127.0.0.1:27017
六月 20, 2017 4:48:36 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:25, serverValue:60}] to 127.0.0.1:27017
----pack out---:MessagePack [_flag=6, _code=18, _messageId=447,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=3, _code=2, _messageId=448,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=3, _code=2, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":0},resentCount=0]
----pack in---:MessagePack [_flag=1, _code=8, _messageId=449,reserved=0, _version=0, _statusCode=0, ack=0, _data={"deviceId":"A100005C51F04B","platform":4,"pushType":1,"token":"K4CshedTSLj++zrCj2CytOF2B6ziwLqYv+4clsBUQCg=","uid":"100"},resentCount=0]
----pack out---:MessagePack [_flag=1, _code=8, _messageId=449,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=1, _code=8, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=3, _code=2, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=1, _code=8, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=11, _code=2, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=0, _data={"insert":[],"update":[],"delete":[],"maxIdentity":1496824323778},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=18, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=0, _data=[{"to":"24","count":0}],resentCount=0]
----pack in---:MessagePack [_flag=11, _code=2, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=6, _code=18, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=6, _code=13, _messageId=450,reserved=0, _version=0, _statusCode=0, ack=0, _data={"length":1,"queryId":"24","updateId":0},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=13, _messageId=450,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=6, _code=13, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=0, _data={"datas":[{"messageCode":3,"receiptNum":69,"lastReceiptTime":0,"readState":1,"msgId":"fa8532ea0174833525aa9175315189c6","from":"100025","to":"24","type":5,"content":"{\"text\":\"测试\",\"style\":\"\",\"act\":\"0\"}","timestamp":1493796383071,"shouldRecvNum":69}],"updateId":1497948516511},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=13, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=6, _code=17, _messageId=7,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[],"revokes":[],"datas":[{"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"0700c8a6920a70e47e77dc4ed17d7e53","from":"99","to":"100","type":5,"content":"{\"text\":\"ni那你呢\"}","timestamp":1497932861969,"shouldRecvNum":1},{"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"794205fe5775a0ddd549971541ce39b8","from":"99","to":"100","type":5,"content":"{\"text\":\"测试\"}","timestamp":1497932832863,"shouldRecvNum":1},{"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"e4a9ee80bfbcea9f72a59217c32d47cf","from":"99","to":"100","type":5,"content":"{\"text\":\"测试\"}","timestamp":1497929188951,"shouldRecvNum":1},{"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"cd43b91569e6b09e558411befa7667c0","from":"99","to":"100","type":5,"content":"{\"text\":\"11\"}","timestamp":1497929187121,"shouldRecvNum":1},{"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"c0ff7aa2435a1c267cf7cdc2de64ae0c","from":"99","to":"100","type":5,"content":"{\"text\":\"������\"}","timestamp":1497928153624,"shouldRecvNum":1},{"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"479c45e347e6d9d7b8233ace2f155ce2","from":"99","to":"100","type":5,"content":"{\"text\":\"ce\"}","timestamp":1497928147981,"shouldRecvNum":1},{"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"7d3b42953f036b3b74c3a06562479005","from":"99","to":"100","type":5,"content":"{\"text\":\"���\"}","timestamp":1497927492293,"shouldRecvNum":1},{"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"ec78432f469652ebcb964d6b75d84d67","from":"99","to":"100","type":5,"content":"{\"text\":\"������\"}","timestamp":1497927457906,"shouldRecvNum":1}],"updateId":1497932861969},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=17, _messageId=7,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=1, _code=2, _messageId=8,reserved=0, _version=0, _statusCode=0, ack=0, _data={"status":0,"mStatus":0,"webStatus":0,"uid":"100"},resentCount=0]
----pack in---:MessagePack [_flag=1, _code=2, _messageId=8,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


账户验证请求：登陆账号 登陆密码
----pack in---:MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=0, _data={"device_id":"49E34C022874CB035EFB2052674DAFA9","platform":3,"uid":"99","company_id":10002,"php_version":"v1.6.0","sig":"bbd781af9d8bf797cd69659e0fa833f01e4834ea","state":4},resentCount=0]
2017-06-20 15:27:12,661 (BaseRPC.java:32) INFO  com.shaozi.data.rpc.base.BaseRPC - sz-versionv1.6.0,url:http://dev.t.u.shaozi.com/Server/Auth
----pack out---:MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
2017-06-20 15:27:14,611 (AccountProcessorAdapter.java:244) WARN  com.shaozi.im.business.adapter.processor.AccountProcessorAdapter - rpc request(check):2015(ms)
----pack out---:MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=0, _data={"code":0,"key":"8e99ea31daf876762525ab0822b92e06","onlineState":{"status":4,"mStatus":0,"webStatus":0,"uid":"99"}},resentCount=0]
----pack in---:MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


code : 7 获取在线状态列表
----pack in---:MessagePack [_flag=1, _code=7, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=1, _code=7, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=1, _code=7, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=0, _data={"99":{"status":4,"mStatus":0,"webStatus":0,"uid":"99"}},resentCount=0]
----pack in---:MessagePack [_flag=1, _code=7, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


#获取公司历史消息 公司广播
----pack in---:MessagePack [_flag=6, _code=13, _messageId=498,reserved=0, _version=0, _statusCode=0, ack=0, _data={"length":1,"queryId":"24","updateId":0},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=13, _messageId=498,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=6, _code=13, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=0, _data={"datas":[{"messageCode":3,"receiptNum":69,"lastReceiptTime":0,"readState":1,"msgId":"fa8532ea0174833525aa9175315189c6","from":"100025","to":"24","type":5,"content":"{\"text\":\"测试\",\"style\":\"\",\"act\":\"0\"}","timestamp":1493796383071,"shouldRecvNum":69}],"updateId":1497951006032},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=13, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

批量已读（批量广播）
----pack in---:MessagePack [_flag=6, _code=22, _messageId=81,reserved=0, _version=0, _statusCode=0, ack=0, _data={"sourceId":24,"messageCode":3},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=22, _messageId=81,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 20, 2017 5:38:12 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:38, serverValue:78}] to 127.0.0.1:27017
----pack out---:MessagePack [_flag=6, _code=22, _messageId=14,reserved=0, _version=0, _statusCode=0, ack=0, _data={"sourceId":"24","messageCode":3,"updateId":1497951492036},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=22, _messageId=14,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

code:18 获取未读消息数量
----pack in---:MessagePack [_flag=6, _code=18, _messageId=82,reserved=0, _version=0, _statusCode=0, ack=0, _data={"tos":["24"]},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=18, _messageId=82,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=6, _code=18, _messageId=15,reserved=0, _version=0, _statusCode=0, ack=0, _data=[{"to":"24","count":0}],resentCount=0]
----pack in---:MessagePack [_flag=6, _code=18, _messageId=15,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

----pack in---:MessagePack [_flag=6, _code=13, _messageId=83,reserved=0, _version=0, _statusCode=0, ack=0, _data={"length":20,"updateId":1497951494394,"queryId":24},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=13, _messageId=83,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=6, _code=13, _messageId=16,reserved=0, _version=0, _statusCode=0, ack=0, _data={"datas":[{"messageCode":3,"receiptNum":69,"lastReceiptTime":0,"readState":1,"msgId":"fa8532ea0174833525aa9175315189c6","from":"100025","to":"24","type":5,"content":"{\"text\":\"测试\",\"style\":\"\",\"act\":\"0\"}","timestamp":1493796383071,"shouldRecvNum":69},{"messageCode":3,"receiptNum":69,"lastReceiptTime":0,"readState":1,"msgId":"d9ba880a7db7d532127310373023d444","from":"100039","to":"24","type":5,"content":"{\"text\":\"测试\\n\",\"style\":\"\",\"act\":\"0\"}","timestamp":1493689086767,"shouldRecvNum":69},{"messageCode":3,"receiptNum":69,"lastReceiptTime":0,"readState":1,"msgId":"1d1ff57cb25c40abd9be4942524b4c2d","from":"100021","to":"24","type":5,"content":"{\"text\":\"5.1放假时间4月30日到5月2日！\"}","timestamp":1493457950546,"shouldRecvNum":69},{"messageCode":3,"receiptNum":70,"lastReceiptTime":0,"readState":1,"msgId":"bf2cf907b803d7fde1c49e8d1329c4a6","from":"100018","to":"24","type":5,"content":"{\"text\":\"3点开会\",\"style\":\"\",\"act\":\"0\"}","timestamp":1492673451297,"shouldRecvNum":70},{"messageCode":3,"receiptNum":70,"lastReceiptTime":0,"readState":1,"msgId":"1638d0f01b96aaf8e78f52fb16f9c85f","from":"100018","to":"24","type":5,"content":"{\"text\":\"12132\",\"style\":\"\",\"act\":\"0\"}","timestamp":1492673438583,"shouldRecvNum":70},{"messageCode":3,"receiptNum":70,"lastReceiptTime":0,"readState":1,"msgId":"a4384972aea66b95bfe29235bd068c8d","from":"100005","to":"24","type":5,"content":"{\"text\":\"“三八”妇女节女生放假半天通知：\\n\\n　　　根据国家法定节假日规定，三月八日下午女职工放假半天，请各部门的女职工做好工作安排。\\n\\n\\n                                                                                行政部\\n                                                                              2017年3月7日\",\"style\":\"\",\"act\":\"0\"}","timestamp":1492071945625,"shouldRecvNum":70},{"messageCode":3,"receiptNum":70,"lastReceiptTime":0,"readState":1,"msgId":"ac461cf8a9efe65f5ef13de03d54aed0","from":"100020","to":"24","type":5,"content":"{\"text\":\"明天下午五点，公司聚餐，请大家提前将工作做好。\",\"style\":\"\",\"act\":\"0\"}","timestamp":1492069847760,"shouldRecvNum":70}],"updateId":1497951494394},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=13, _messageId=16,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


android 第一次请求数据
六月 21, 2017 10:52:58 上午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:12, serverValue:155}] to 127.0.0.1:27017
2017-06-21 10:52:58,630 (BaseRPC.java:32) INFO  com.shaozi.data.rpc.base.BaseRPC - sz-versionv1.5.0,url:http://dev.t.u.shaozi.com/Server/Auth
Wed Jun 21 10:52:58 CST 2017:----pack out---:MessagePack [_flag=9, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Wed Jun 21 10:52:58 CST 2017:----pack out---:MessagePack [_flag=1, _code=1, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
2017-06-21 10:53:00,637 (AccountProcessorAdapter.java:244) WARN  com.shaozi.im.business.adapter.processor.AccountProcessorAdapter - rpc request(check):2010(ms)
Wed Jun 21 10:53:00 CST 2017:----pack out---:MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=0, _data={"code":0,"key":"a0d38c4d12c8ce9697923e34c7181824","onlineState":{"status":0,"mStatus":4,"webStatus":0,"uid":"100"}},resentCount=0]
Wed Jun 21 10:53:00 CST 2017:----pack out---:MessagePack [_flag=1, _code=2, _messageId=14,reserved=0, _version=0, _statusCode=0, ack=0, _data={"status":0,"mStatus":4,"webStatus":0,"uid":"100"},resentCount=0]
Wed Jun 21 10:53:00 CST 2017:----pack in---:MessagePack [_flag=1, _code=2, _messageId=14,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Wed Jun 21 10:53:00 CST 2017:----pack in---:MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Wed Jun 21 10:53:00 CST 2017:----pack in---:MessagePack [_flag=11, _code=2, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":0},resentCount=0]
Wed Jun 21 10:53:00 CST 2017:----pack in---:MessagePack [_flag=6, _code=17, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":0},resentCount=0]
Wed Jun 21 10:53:00 CST 2017:----pack out---:MessagePack [_flag=11, _code=2, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Wed Jun 21 10:53:00 CST 2017:----pack in---:MessagePack [_flag=3, _code=2, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":0},resentCount=0]
六月 21, 2017 10:53:01 上午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:13, serverValue:157}] to 127.0.0.1:27017
六月 21, 2017 10:53:01 上午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:14, serverValue:156}] to 127.0.0.1:27017
Wed Jun 21 10:53:01 CST 2017:----pack out---:MessagePack [_flag=6, _code=17, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack out---:MessagePack [_flag=3, _code=2, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack out---:MessagePack [_flag=11, _code=2, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=0, _data={"insert":[{"gName":"哨子办公","gNPinyin":"SHAOZIBANGONG,","gNPYHead":"SZBG,","groupId":"4c9a0d2ab3767976284b98dafe1b1dda","creator":"99","groupType":4,"lastUpdateTime":1493966756453,"createTime":1492068457513,"members":["100060","100061","100062","100063","100020","100064","100065","100021","100066","100022","100056","100012","100057","100013","100058","100014","100059","100015","100016","100017","100018","100019","99","100031","100032","100033","100067","100023","100024","100068","100025","100069","100026","100027","100028","100029","100040","100041","100042","100043","100044","100000","100034","100035","100036","100037","100038","100039","100050","100051","100052","100053","100054","100010","100055","100011","100009","100","100045","100001","100002","100046","100047","100003","100048","100004","100049","100006","100007","100008"]},{"gName":"财务部","gNPinyin":"CAIWUBU,","gNPYHead":"CWB,","groupId":"22088e9c1488ff356315908371609913","creator":"100044","groupType":3,"lastUpdateTime":1493301417747,"createTime":1492068680672,"members":["100","100044"]},{"gName":"巨融文化传媒运营中心","gNPinyin":"JURONGWENHUAZHUANMEIYUNYINGZHONGXIN,JURONGWENHUACHUANMEIYUNYINGZHONGXIN,","gNPYHead":"JRWHCMYYZX,JRWHZMYYZX,","groupId":"338a995399dee59dd101b91a3cc2b814","creator":"100060","groupType":1,"lastUpdateTime":1496645252501,"createTime":1492536414217,"members":["100060","100061","100062","100063","100020","100064","100021","100066","100022","100056","100012","100057","100013","100058","100014","100059","100015","100016","100017","100018","100019","99","100030","100031","100032","100033","100067","100023","100068","100024","100025","100026","100028","100029","100040","100041","100043","100000","100044","100034","100035","100036","100037","100038","100039","100050","100051","100053","100054","100010","100055","100011","100009","100","100001","100045","100002","100046","100047","100003","100048","100004","100005","100049","100006","100007","100008"]},{"gName":"马祥,陈璐荷,尚文清,王银喜,杨海清,杨...","gNPinyin":"MAXIANG,CHENLUHE,SHANGWENQING,WANGYINXI,YANGHAIQING,YANG...,","gNPYHead":"MX,CLH,SWQ,WYX,YHQ,Y...,","groupId":"6477d3797afc520c1fd410a31a651717","creator":"100016","groupType":1,"lastUpdateTime":1494595356255,"createTime":1492672064544,"members":["100","100000","100001","100016","100005"]},{"gName":"尚文清,杨海清,王银喜,申根换 等...","gNPinyin":"SHANGWENQING,YANGHAIQING,WANGYINXI,SHENGENHUAN DENG...,","gNPYHead":"SWQ,YHQ,WYX,SGH D...,","groupId":"ebe51e6106c006ddf5dc72b4d1e36f11","creator":"100059","groupType":1,"lastUpdateTime":1492772719310,"createTime":1492772719309,"members":["100","100001","100059","100005","100018"]},{"gName":"行政部门","gNPinyin":"XINGZHENGBUMEN,HANGZHENGBUMEN,HENGZHENGBUMEN,","gNPYHead":"XZBM,HZBM,","groupId":"e9f9d334997ee4183cd75b42489c1862","creator":"25","groupType":3,"lastUpdateTime":1493806152348,"createTime":1493607353029,"members":["100","100044","100069"]},{"gName":"安全部门","gNPinyin":"ANQUANBUMEN,","gNPYHead":"AQBM,","groupId":"0e1e05de66ab9da037401ceb0a6b315a","creator":"100","groupType":3,"lastUpdateTime":1493806152358,"createTime":1493607482812,"members":["100","100044","100069"]},{"gName":"尚文清,王二锁,王志宏,戴双宝 等...","gNPinyin":"SHANGWENQING,WANGERSUO,WANGZHIHONG,DAISHUANGBAO DENG...,","gNPYHead":"SWQ,WES,WZH,DSB D...,","groupId":"9a50170816a783410ccfeb37f79c2f90","creator":"100027","groupType":1,"lastUpdateTime":1494824505479,"createTime":1494824505477,"members":["100","100033","100023","100024","100027"]},{"gName":"孙瑞军,尚文清,王越建,冯州龙,孙瑞军","gNPinyin":"SUNRUIJUN,SHANGWENQING,WANGYUEJIAN,PINGZHOULONG,SUNRUIJUN,SUNRUIJUN,SHANGWENQING,WANGYUEJIAN,FENGZHOULONG,SUNRUIJUN,","gNPYHead":"SRJ,SWQ,WYJ,PZL,SRJ,SRJ,SWQ,WYJ,FZL,SRJ,","groupId":"db2f8024c23b62941e4b44a15e09562a","creator":"100029","groupType":1,"lastUpdateTime":1496241607660,"createTime":1496241607629,"members":["100","100051","100002","100029"]}],"update":[],"delete":[{"quitType":2,"gName":"王飞云,尚文清,冯州龙,王越建,杜文渊,...","gNPinyin":"WANGFEIYUN,SHANGWENQING,PINGZHOULONG,WANGYUEJIAN,DUWENYUAN,...,WANGFEIYUN,SHANGWENQING,FENGZHOULONG,WANGYUEJIAN,DUWENYUAN,...,","gNPYHead":"WFY,SWQ,PZL,WYJ,DWY,...,WFY,SWQ,FZL,WYJ,DWY,...,","groupId":"0d3edd52bfe0e26bb7ae3a5656a03e18","creator":"100004","groupType":1,"lastUpdateTime":1496824323757,"createTime":1494503707321,"members":[]}],"maxIdentity":1496824323778},resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack out---:MessagePack [_flag=3, _code=2, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":0},resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack in---:MessagePack [_flag=6, _code=18, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=0, _data={"tos":["24"]},resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack in---:MessagePack [_flag=1, _code=8, _messageId=7,reserved=0, _version=0, _statusCode=0, ack=0, _data={"deviceId":"A100005C51F04B","platform":4,"pushType":1,"token":"uGB+Wj62Wgb+AnHWrXVy8Gq3GoiilVL/ucL5YplUCUg=","uid":"100"},resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack out---:MessagePack [_flag=6, _code=18, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack out---:MessagePack [_flag=1, _code=8, _messageId=7,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack out---:MessagePack [_flag=1, _code=8, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack out---:MessagePack [_flag=6, _code=18, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=0, _data=[{"to":"24","count":0}],resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack in---:MessagePack [_flag=11, _code=2, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack out---:MessagePack [_flag=6, _code=17, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=0, _data={"revokes":[],"datas":[{"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"ec78432f469652ebcb964d6b75d84d67","from":"99","to":"100","type":5,"content":"{\"text\":\"������\"}","timestamp":1497927457906,"shouldRecvNum":1},{"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"f17ededc9bcab5ea663d9732dfc8439e","from":"99","to":"100","type":5,"content":"{\"text\":\"你好\"}","timestamp":1497925161529,"shouldRecvNum":1},{"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"31559bbe7f3b535590b3962fd2de49f6","from":"100040","to":"100","type":5,"content":"{\"text\":\"测试\"}","timestamp":1497517317863,"shouldRecvNum":1},{"messageCode":2,"receiptNum":9,"lastReceiptTime":0,"readState":0,"msgId":"7a0050186222ac66e8f90f31919c045d","from":"100027","to":"4c9a0d2ab3767976284b98dafe1b1dda","type":5,"content":"{\"text\":\"？\"}","timestamp":1497515338432,"shouldRecvNum":69},{"messageCode":2,"receiptNum":11,"lastReceiptTime":0,"readState":0,"msgId":"82b5797566657c2edbad250c6157e630","from":"100029","to":"4c9a0d2ab3767976284b98dafe1b1dda","type":5,"content":"{\"text\":\"😓\"}","timestamp":1497514951933,"shouldRecvNum":69},{"messageCode":2,"receiptNum":11,"lastReceiptTime":0,"readState":0,"msgId":"9568c934d79b90f967c92385eb4f808a","from":"100029","to":"4c9a0d2ab3767976284b98dafe1b1dda","type":53,"content":"{\"mapType\":1,\"lat\":\"39.982202\",\"title\":\"北京市海淀区海淀南路31号院116室\",\"lon\":\"116.311198\",\"text\":\"北京市海淀区海淀南路31号院116室\"}","timestamp":1497514941932,"shouldRecvNum":69},{"messageCode":2,"receiptNum":24,"lastReceiptTime":0,"readState":0,"msgId":"dbf8a2ff37d5e2c421d8dc6956644c22","from":"100056","to":"4c9a0d2ab3767976284b98dafe1b1dda","type":5,"content":"{\"text\":\"好的\"}","timestamp":1497493416881,"shouldRecvNum":69},{"messageCode":2,"receiptNum":23,"lastReceiptTime":0,"readState":0,"msgId":"9ceb59745feb7f5e7d14bf838fb0734d","from":"100056","to":"4c9a0d2ab3767976284b98dafe1b1dda","type":49,"content":"{\"noticeId\":\"5928d15ae3900f3a0df6e515\",\"noticeType\":3,\"title\":\"111\"}","timestamp":1497493409985,"shouldRecvNum":52},{"messageCode":2,"receiptNum":25,"lastReceiptTime":0,"readState":0,"msgId":"da83fae7d37c83fae248910934b17adb","from":"100050","to":"4c9a0d2ab3767976284b98dafe1b1dda","type":49,"content":"{\"noticeType\":3,\"title\":\"111\",\"noticeId\":\"5928d15ae3900f3a0df6e515\"}","timestamp":1497491396196,"shouldRecvNum":53}],"updateId":1498013580968},resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack in---:MessagePack [_flag=3, _code=2, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack in---:MessagePack [_flag=1, _code=8, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack in---:MessagePack [_flag=6, _code=18, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack in---:MessagePack [_flag=6, _code=13, _messageId=8,reserved=0, _version=0, _statusCode=0, ack=0, _data={"length":1,"queryId":"24","updateId":0},resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack out---:MessagePack [_flag=6, _code=13, _messageId=8,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack out---:MessagePack [_flag=6, _code=13, _messageId=7,reserved=0, _version=0, _statusCode=0, ack=0, _data={"datas":[{"messageCode":3,"receiptNum":69,"lastReceiptTime":0,"readState":1,"msgId":"fa8532ea0174833525aa9175315189c6","from":"100025","to":"24","type":5,"content":"{\"text\":\"测试\",\"style\":\"\",\"act\":\"0\"}","timestamp":1493796383071,"shouldRecvNum":69}],"updateId":1498013581305},resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack in---:MessagePack [_flag=6, _code=17, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Wed Jun 21 10:53:01 CST 2017:----pack in---:MessagePack [_flag=6, _code=13, _messageId=7,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]



code : 8 更新mobile的推送token
----pack in---:MessagePack [_flag=1, _code=8, _messageId=449,reserved=0, _version=0, _statusCode=0, ack=0, _data={"deviceId":"A100005C51F04B","platform":4,"pushType":1,"token":"K4CshedTSLj++zrCj2CytOF2B6ziwLqYv+4clsBUQCg=","uid":"100"},resentCount=0]
----pack out---:MessagePack [_flag=1, _code=8, _messageId=449,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=1, _code=8, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=1, _code=8, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

 获取未读消息数量

 ----pack in---:MessagePack [_flag=6, _code=18, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=0, _data={"tos":["24"]},resentCount=0]
 ----pack out---:MessagePack [_flag=6, _code=18, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
 ----pack out---:MessagePack [_flag=6, _code=18, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=0, _data=[{"to":"24","count":0}],resentCount=0]
 ----pack in---:MessagePack [_flag=6, _code=18, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


合并离线消息（个人，群组，公司，回执 合并）code: 17
----pack in---:MessagePack [_flag=6, _code=17, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":1497932861969},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=17, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=6, _code=17, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[],"revokes":[],"datas":[],"updateId":1497932861969},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=17, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


获取群信息
----pack in---:MessagePack [_flag=11, _code=2, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":1496824323778},resentCount=0]
----pack out---:MessagePack [_flag=11, _code=2, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=11, _code=2, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=0, _data={"insert":[],"update":[],"delete":[],"maxIdentity":1496824323778},resentCount=0]
----pack in---:MessagePack [_flag=11, _code=2, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


用户群组设置
----pack in---:MessagePack [_flag=3, _code=1, _messageId=31,reserved=0, _version=0, _statusCode=0, ack=0, _data={"chatId":"83c7133fb39a320de58a5fe6a9b6f857","messageCode":2,"add":[{"quiet":true}]},resentCount=0]
六月 20, 2017 4:18:51 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:15, serverValue:48}] to 127.0.0.1:27017
----pack out---:MessagePack [_flag=3, _code=1, _messageId=31,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=3, _code=1, _messageId=8,reserved=0, _version=0, _statusCode=0, ack=0, _data={"setting":{"quiet":true},"updateId":1497946731596,"messageCode":2,"chatId":"83c7133fb39a320de58a5fe6a9b6f857","isDelete":0},resentCount=0]
----pack in---:MessagePack [_flag=3, _code=1, _messageId=8,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


----pack in---:MessagePack [_flag=3, _code=1, _messageId=36,reserved=0, _version=0, _statusCode=0, ack=0, _data={"chatId":"83c7133fb39a320de58a5fe6a9b6f857","messageCode":2,"del":["quiet"]},resentCount=0]
六月 20, 2017 4:23:25 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:17, serverValue:50}] to 127.0.0.1:27017
2017-06-20 16:23:26,067 (UserChatGroupSettingMDao.java:59) INFO  com.shaozi.im.business.data.mongodao.UserChatGroupSettingMDao - save cache:key:83c7133fb39a320de58a5fe6a9b6f857_99_2
----pack out---:MessagePack [_flag=3, _code=1, _messageId=36,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=3, _code=1, _messageId=9,reserved=0, _version=0, _statusCode=0, ack=0, _data={"setting":{},"updateId":1497947006063,"messageCode":2,"chatId":"83c7133fb39a320de58a5fe6a9b6f857","isDelete":0},resentCount=0]
----pack in---:MessagePack [_flag=3, _code=1, _messageId=9,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


----pack in---:MessagePack [_flag=3, _code=2, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":1497947006063},resentCount=0]
六月 20, 2017 4:26:10 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:19, serverValue:52}] to 127.0.0.1:27017
----pack out---:MessagePack [_flag=3, _code=2, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=3, _code=2, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":1497947006063},resentCount=0]
----pack in---:MessagePack [_flag=3, _code=2, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

Query: { "isDelete" : 0 , "updateId" : { "$gt" : 0} , "userId" : "99"}, Fields: null, Sort: { "updateId" : 1}

用户心跳
----pack in---:MessagePack [_flag=9, _code=1, _messageId=14,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=9, _code=1, _messageId=14,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


聊天窗口 已读未读

----pack in---:MessagePack [_flag=6, _code=20, _messageId=517,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"content":"{\"receiptMsgId\":\"7d3b42953f036b3b74c3a06562479005\",\"receiptTo\":\"100\",\"receiptType\":1}","device":"A100005C51F04B","from":"100","msgId":"ef566c18071d4ed092aa8b559571acc7","readState":1,"to":"99"},{"content":"{\"receiptMsgId\":\"479c45e347e6d9d7b8233ace2f155ce2\",\"receiptTo\":\"100\",\"receiptType\":1}","device":"A100005C51F04B","from":"100","msgId":"66836a32f6704a14b232e5b450c7d018","readState":1,"to":"99"},{"content":"{\"receiptMsgId\":\"c0ff7aa2435a1c267cf7cdc2de64ae0c\",\"receiptTo\":\"100\",\"receiptType\":1}","device":"A100005C51F04B","from":"100","msgId":"0be635fa49fe4ed89593fd442baec519","readState":1,"to":"99"},{"content":"{\"receiptMsgId\":\"cd43b91569e6b09e558411befa7667c0\",\"receiptTo\":\"100\",\"receiptType\":1}","device":"A100005C51F04B","from":"100","msgId":"7f73bef6d0554419b944c4dcdfb83fd9","readState":1,"to":"99"},{"content":"{\"receiptMsgId\":\"e4a9ee80bfbcea9f72a59217c32d47cf\",\"receiptTo\":\"100\",\"receiptType\":1}","device":"A100005C51F04B","from":"100","msgId":"8d42128949c54a8685794870d4354fec","readState":1,"to":"99"},{"content":"{\"receiptMsgId\":\"794205fe5775a0ddd549971541ce39b8\",\"receiptTo\":\"100\",\"receiptType\":1}","device":"A100005C51F04B","from":"100","msgId":"d08c9241a0e04c43beda431639f53d93","readState":1,"to":"99"},{"content":"{\"receiptMsgId\":\"0700c8a6920a70e47e77dc4ed17d7e53\",\"receiptTo\":\"100\",\"receiptType\":1}","device":"A100005C51F04B","from":"100","msgId":"35be79b171a24a53b93308da04735b80","readState":1,"to":"99"}]},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=20, _messageId=517,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 20, 2017 5:46:59 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:42, serverValue:82}] to 127.0.0.1:27017
----pack out---:MessagePack [_flag=6, _code=20, _messageId=26,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"messageCode":0,"receiptNum":1,"lastReceiptTime":0,"readState":1,"msgId":"7d3b42953f036b3b74c3a06562479005","from":"100","to":"99","type":0,"content":"{\"receiptMsgId\":\"7d3b42953f036b3b74c3a06562479005\",\"receiptNum\":1,\"receiptTo\":\"100\",\"receiptType\":1,\"readState\":1}","timestamp":1497952019789,"device":"A100005C51F04B","fromIp":167974322,"fromPort":60817,"shouldRecvNum":0,"oldMsgId":"ef566c18071d4ed092aa8b559571acc7"},{"messageCode":0,"receiptNum":1,"lastReceiptTime":0,"readState":1,"msgId":"479c45e347e6d9d7b8233ace2f155ce2","from":"100","to":"99","type":0,"content":"{\"receiptMsgId\":\"479c45e347e6d9d7b8233ace2f155ce2\",\"receiptNum\":1,\"receiptTo\":\"100\",\"receiptType\":1,\"readState\":1}","timestamp":1497952019789,"device":"A100005C51F04B","fromIp":167974322,"fromPort":60817,"shouldRecvNum":0,"oldMsgId":"66836a32f6704a14b232e5b450c7d018"},{"messageCode":0,"receiptNum":1,"lastReceiptTime":0,"readState":1,"msgId":"c0ff7aa2435a1c267cf7cdc2de64ae0c","from":"100","to":"99","type":0,"content":"{\"receiptMsgId\":\"c0ff7aa2435a1c267cf7cdc2de64ae0c\",\"receiptNum\":1,\"receiptTo\":\"100\",\"receiptType\":1,\"readState\":1}","timestamp":1497952019789,"device":"A100005C51F04B","fromIp":167974322,"fromPort":60817,"shouldRecvNum":0,"oldMsgId":"0be635fa49fe4ed89593fd442baec519"},{"messageCode":0,"receiptNum":1,"lastReceiptTime":0,"readState":1,"msgId":"cd43b91569e6b09e558411befa7667c0","from":"100","to":"99","type":0,"content":"{\"receiptMsgId\":\"cd43b91569e6b09e558411befa7667c0\",\"receiptNum\":1,\"receiptTo\":\"100\",\"receiptType\":1,\"readState\":1}","timestamp":1497952019789,"device":"A100005C51F04B","fromIp":167974322,"fromPort":60817,"shouldRecvNum":0,"oldMsgId":"7f73bef6d0554419b944c4dcdfb83fd9"},{"messageCode":0,"receiptNum":1,"lastReceiptTime":0,"readState":1,"msgId":"e4a9ee80bfbcea9f72a59217c32d47cf","from":"100","to":"99","type":0,"content":"{\"receiptMsgId\":\"e4a9ee80bfbcea9f72a59217c32d47cf\",\"receiptNum\":1,\"receiptTo\":\"100\",\"receiptType\":1,\"readState\":1}","timestamp":1497952019789,"device":"A100005C51F04B","fromIp":167974322,"fromPort":60817,"shouldRecvNum":0,"oldMsgId":"8d42128949c54a8685794870d4354fec"},{"messageCode":0,"receiptNum":1,"lastReceiptTime":0,"readState":1,"msgId":"794205fe5775a0ddd549971541ce39b8","from":"100","to":"99","type":0,"content":"{\"receiptMsgId\":\"794205fe5775a0ddd549971541ce39b8\",\"receiptNum\":1,\"receiptTo\":\"100\",\"receiptType\":1,\"readState\":1}","timestamp":1497952019789,"device":"A100005C51F04B","fromIp":167974322,"fromPort":60817,"shouldRecvNum":0,"oldMsgId":"d08c9241a0e04c43beda431639f53d93"},{"messageCode":0,"receiptNum":1,"lastReceiptTime":0,"readState":1,"msgId":"0700c8a6920a70e47e77dc4ed17d7e53","from":"100","to":"99","type":0,"content":"{\"receiptMsgId\":\"0700c8a6920a70e47e77dc4ed17d7e53\",\"receiptNum\":1,\"receiptTo\":\"100\",\"receiptType\":1,\"readState\":1}","timestamp":1497952019789,"device":"A100005C51F04B","fromIp":167974322,"fromPort":60817,"shouldRecvNum":0,"oldMsgId":"35be79b171a24a53b93308da04735b80"}],"updateId":1497952019789},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=20, _messageId=26,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


----pack in---:MessagePack [_flag=6, _code=20, _messageId=597,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"content":"{\"receiptMsgId\":\"71181b84f90eb65844905e0d65c5d49f\",\"receiptTo\":\"100\",\"receiptType\":1}","device":"A100005C51F04B","from":"100","msgId":"a70c18c1fc04485b8bc1f8a0136b6162","readState":1,"to":"99"}]},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=20, _messageId=597,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 20, 2017 7:16:19 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:57, serverValue:103}] to 127.0.0.1:27017
----pack out---:MessagePack [_flag=6, _code=20, _messageId=7,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"messageCode":0,"receiptNum":1,"lastReceiptTime":0,"readState":1,"msgId":"71181b84f90eb65844905e0d65c5d49f","from":"100","to":"99","type":0,"content":"{\"receiptMsgId\":\"71181b84f90eb65844905e0d65c5d49f\",\"receiptNum\":1,\"receiptTo\":\"100\",\"receiptType\":1,\"readState\":1}","timestamp":1497957379003,"device":"A100005C51F04B","fromIp":167974322,"fromPort":60820,"shouldRecvNum":0,"oldMsgId":"a70c18c1fc04485b8bc1f8a0136b6162"}],"updateId":1497957379003},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=20, _messageId=7,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


群组拉历史消息
----pack out---:MessagePack [_flag=9, _code=1, _messageId=604,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=6, _code=12, _messageId=18,reserved=0, _version=0, _statusCode=0, ack=0, _data={"length":20,"updateId":1497442389819,"queryId":"83c7133fb39a320de58a5fe6a9b6f857"},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=12, _messageId=18,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 20, 2017 7:23:08 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:59, serverValue:106}] to 127.0.0.1:27017
----pack out---:MessagePack [_flag=6, _code=12, _messageId=8,reserved=0, _version=0, _statusCode=0, ack=0, _data={"datas":[{"messageCode":2,"receiptNum":20,"lastReceiptTime":0,"readState":0,"msgId":"fa8e68a624b4463a1a956eae38f0b9e5","from":"99","to":"83c7133fb39a320de58a5fe6a9b6f857","type":5,"content":"{\"text\":\"1\"}","timestamp":1497437602862,"shouldRecvNum":47},{"messageCode":2,"receiptNum":18,"lastReceiptTime":0,"readState":1,"msgId":"40855c5581ecf74b8dd45c5652290a4e","from":"100064","to":"83c7133fb39a320de58a5fe6a9b6f857","type":49,"content":"{\"noticeId\":\"5937af57e3900fd334f6e519\",\"noticeType\":3,\"title\":\"下午好\"}","timestamp":1497433163738,"shouldRecvNum":39},{"messageCode":2,"receiptNum":23,"lastReceiptTime":0,"readState":1,"msgId":"0b3e976c47690a8139723cb1c66a2415","from":"100033","to":"83c7133fb39a320de58a5fe6a9b6f857","type":49,"content":"{\"noticeId\":\"5937af57e3900fd334f6e519\",\"noticeType\":3,\"title\":\"下午好\"}","timestamp":1497419547845,"shouldRecvNum":40},{"messageCode":2,"receiptNum":35,"lastReceiptTime":0,"readState":1,"msgId":"8a76e1bdec361f01597b7db09bab450b","from":"100016","to":"83c7133fb39a320de58a5fe6a9b6f857","type":5,"content":"{\"text\":\"额\"}","timestamp":1497327905486,"shouldRecvNum":47},{"messageCode":2,"receiptNum":29,"lastReceiptTime":0,"readState":1,"msgId":"8d14bc5c8a638c1dcf41ff2835108809","from":"100009","to":"83c7133fb39a320de58a5fe6a9b6f857","type":49,"content":"{\"noticeType\":3,\"title\":\"下午好\",\"noticeId\":\"5937af57e3900fd334f6e519\"}","timestamp":1497326148017,"shouldRecvNum":41},{"messageCode":2,"receiptNum":35,"lastReceiptTime":0,"readState":1,"msgId":"43cc509cf2420ef7942d8f7e2c3eda90","from":"100035","to":"83c7133fb39a320de58a5fe6a9b6f857","type":49,"content":"{\"noticeId\":\"5937af57e3900fd334f6e519\",\"noticeType\":3,\"title\":\"下午好\"}","timestamp":1497266123682,"shouldRecvNum":42},{"messageCode":2,"receiptNum":37,"lastReceiptTime":0,"readState":1,"msgId":"0eaf92c34b677f8ced8f685b07bfccfa","from":"100013","to":"83c7133fb39a320de58a5fe6a9b6f857","type":49,"content":"{\"noticeId\":\"5937af57e3900fd334f6e519\",\"noticeType\":3,\"title\":\"下午好\"}","timestamp":1497080038359,"shouldRecvNum":43},{"messageCode":2,"receiptNum":40,"lastReceiptTime":0,"readState":1,"msgId":"4860c96b2016dfe4b0ad8cd8cf7dc51c","from":"100065","to":"83c7133fb39a320de58a5fe6a9b6f857","type":49,"content":"{\"noticeId\":\"5937af57e3900fd334f6e519\",\"noticeType\":3,\"title\":\"下午好\"}","timestamp":1497067813217,"shouldRecvNum":44},{"messageCode":2,"receiptNum":40,"lastReceiptTime":0,"readState":1,"msgId":"a5ce5c38311d79c5fe4f6c394cea7ff9","from":"100057","to":"83c7133fb39a320de58a5fe6a9b6f857","type":49,"content":"{\"noticeId\":\"5937af57e3900fd334f6e519\",\"noticeType\":3,\"title\":\"下午好\"}","timestamp":1496993182216,"shouldRecvNum":45},{"messageCode":2,"receiptNum":43,"lastReceiptTime":0,"readState":1,"msgId":"a796d73f8956fe5c8fbc528e7e38da4f","from":"100059","to":"83c7133fb39a320de58a5fe6a9b6f857","type":49,"content":"{\"noticeType\":3,\"title\":\"下午好\",\"noticeId\":\"5937af57e3900fd334f6e519\"}","timestamp":1496926930649,"shouldRecvNum":46},{"messageCode":2,"receiptNum":42,"lastReceiptTime":0,"readState":1,"msgId":"96062fc3b7142186d0f41496635ae808","from":"100059","to":"83c7133fb39a320de58a5fe6a9b6f857","type":5,"content":"{\"text\":\"什么情况\"}","timestamp":1496926914296,"shouldRecvNum":47},{"messageCode":2,"receiptNum":42,"lastReceiptTime":0,"readState":1,"msgId":"95741294987a5c567ec989fbac19dc47","from":"100024","to":"83c7133fb39a320de58a5fe6a9b6f857","type":49,"content":"{\"noticeType\":3,\"title\":\"下午好\",\"noticeId\":\"5937af57e3900fd334f6e519\"}","timestamp":1496903358236,"shouldRecvNum":47},{"messageCode":2,"receiptNum":41,"lastReceiptTime":0,"readState":1,"msgId":"9a6cd5d440ee9e8927ba9096f9d25d09","from":"100013","to":"83c7133fb39a320de58a5fe6a9b6f857","type":5,"content":"{\"text\":\"这是哪里？\"}","timestamp":1496897529563,"shouldRecvNum":47},{"messageCode":2,"receiptNum":42,"lastReceiptTime":0,"readState":1,"msgId":"57f7a738db23350f60b9daf9ff3e91ac","from":"100064","to":"83c7133fb39a320de58a5fe6a9b6f857","type":5,"content":"{\"text\":\"好\"}","timestamp":1496821716475,"shouldRecvNum":47},{"messageCode":2,"receiptNum":42,"lastReceiptTime":0,"readState":1,"msgId":"c63c5e16640fea3c7f3c69d31dd259b7","from":"100068","to":"83c7133fb39a320de58a5fe6a9b6f857","type":49,"content":"{\"noticeId\":\"5937af57e3900fd334f6e519\",\"noticeType\":1,\"text\":\"下午好\"}","timestamp":1496821591679,"shouldRecvNum":47},{"messageCode":2,"receiptNum":41,"lastReceiptTime":0,"readState":1,"msgId":"6f87c333461ad06510a15afa80962831","from":"100064","to":"83c7133fb39a320de58a5fe6a9b6f857","type":5,"content":"{\"text\":\"？？\"}","timestamp":1496821186545,"shouldRecvNum":47},{"messageCode":2,"receiptNum":41,"lastReceiptTime":0,"readState":1,"msgId":"d07da6ff4ca3bb06648880aef563abbd","from":"100004","to":"83c7133fb39a320de58a5fe6a9b6f857","type":5,"content":"{\"text\":\"uk\"}","timestamp":1496625910584,"shouldRecvNum":47},{"messageCode":2,"receiptNum":43,"lastReceiptTime":0,"readState":1,"msgId":"95092b72b7ff869bae2b9c236809dc9c","from":"100000","to":"83c7133fb39a320de58a5fe6a9b6f857","type":5,"content":"{\"text\":\"把钱发给大家的最好\"}","timestamp":1496546253001,"shouldRecvNum":47},{"messageCode":2,"receiptNum":33,"lastReceiptTime":0,"readState":1,"msgId":"8bd4d8370b6d078ad2f98a239f6e0c13","from":"100000","to":"83c7133fb39a320de58a5fe6a9b6f857","type":49,"content":"{\"noticeId\":\"5912d672e3900fab5033ae64\",\"noticeType\":3,\"title\":\"吃早饭了么\"}","timestamp":1496546221150,"shouldRecvNum":37},{"messageCode":2,"receiptNum":40,"lastReceiptTime":0,"readState":1,"msgId":"bb7a1da2282ec9248b1723494de2fc31","from":"100000","to":"83c7133fb39a320de58a5fe6a9b6f857","type":49,"content":"{\"noticeId\":\"59260fbee3900fd63bf6e514\",\"noticeType\":3,\"title\":\"早上好。\"}","timestamp":1496546212495,"shouldRecvNum":44}],"updateId":1497442389819},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=12, _messageId=8,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=9, _code=1, _messageId=605,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=9, _code=1, _messageId=605,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=9, _code=1, _messageId=19,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=9, _code=1, _messageId=19,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

发群消息
----pack in---:MessagePack [_flag=6, _code=2, _messageId=20,reserved=0, _version=0, _statusCode=0, ack=0, _data={"from":"99","to":"338a995399dee59dd101b91a3cc2b814","type":5,"content":"{\"text\":\"你好呀\"}","msgId":"13c6a4c087f852c048930f7e8c32ec99","device":"49E34C022874CB035EFB2052674DAFA9","spaceSize":9,"timestamp":1497957875811,"text":"你好呀"},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=2, _messageId=20,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 20, 2017 7:24:35 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Closed connection [connectionId{localValue:59, serverValue:106}] to 127.0.0.1:27017 because it is past its maximum allowed idle time.
六月 20, 2017 7:24:35 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:60, serverValue:108}] to 127.0.0.1:27017
2017-06-20 19:24:35,922 (MessageProcessor.java:88) INFO  com.shaozi.im.processors.MessageProcessor - group build chatlog(ms)-:76
----pack out---:MessagePack [_flag=6, _code=2, _messageId=9,reserved=0, _version=0, _statusCode=0, ack=0, _data={"msgId":"14bb3ed11a3e0018385cebdaf38d06af","oldMsgId":"13c6a4c087f852c048930f7e8c32ec99","timestamp":1497957875841,"type":46,"shouldRecvNum":66},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=2, _messageId=9,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
2017-06-20 19:24:36,013 (MessageProcessor.java:93) INFO  com.shaozi.im.processors.MessageProcessor - sendMessageGroup(ms)-:87
----pack out---:MessagePack [_flag=6, _code=2, _messageId=12,reserved=0, _version=0, _statusCode=0, ack=0, _data={"messageCode":2,"receiptNum":0,"lastReceiptTime":0,"readState":0,"sound":"im.wav","msgId":"14bb3ed11a3e0018385cebdaf38d06af","from":"99","to":"338a995399dee59dd101b91a3cc2b814","type":5,"content":"{\"text\":\"你好呀\"}","timestamp":1497957875841,"device":"49E34C022874CB035EFB2052674DAFA9","shouldRecvNum":66,"companyId":"10002","id":"594905f3e8f8f20b93166713"},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=2, _messageId=12,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=9, _code=1, _messageId=606,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=9, _code=1, _messageId=606,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

群里面已读
----pack in---:MessagePack [_flag=9, _code=1, _messageId=609,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=9, _code=1, _messageId=609,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=6, _code=20, _messageId=610,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"content":"{\"receiptMsgId\":\"14bb3ed11a3e0018385cebdaf38d06af\",\"receiptTo\":\"100\",\"receiptType\":2}","device":"A100005C51F04B","from":"100","msgId":"d570b663974447fea0e6bd06a05e1f7a","readState":1,"to":"99"}]},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=20, _messageId=610,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 20, 2017 7:28:45 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:61, serverValue:109}] to 127.0.0.1:27017
----pack out---:MessagePack [_flag=6, _code=20, _messageId=10,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"messageCode":0,"receiptNum":1,"lastReceiptTime":0,"readState":1,"msgId":"14bb3ed11a3e0018385cebdaf38d06af","from":"100","to":"99","type":0,"content":"{\"receiptMsgId\":\"14bb3ed11a3e0018385cebdaf38d06af\",\"receiptNum\":1,\"receiptTo\":\"100\",\"receiptType\":2,\"readState\":1}","timestamp":1497958125625,"device":"A100005C51F04B","fromIp":167974322,"fromPort":60820,"shouldRecvNum":0,"oldMsgId":"d570b663974447fea0e6bd06a05e1f7a"}],"updateId":1497958125625},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=20, _messageId=10,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

点击查看已读 未读
----pack in---:MessagePack [_flag=9, _code=1, _messageId=25,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=9, _code=1, _messageId=25,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=9, _code=1, _messageId=612,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
----pack out---:MessagePack [_flag=9, _code=1, _messageId=612,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=6, _code=8, _messageId=26,reserved=0, _version=0, _statusCode=0, ack=0, _data={"msgId":"14bb3ed11a3e0018385cebdaf38d06af"},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=8, _messageId=26,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 20, 2017 7:29:50 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Closed connection [connectionId{localValue:61, serverValue:109}] to 127.0.0.1:27017 because it is past its maximum allowed idle time.
六月 20, 2017 7:29:50 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:62, serverValue:111}] to 127.0.0.1:27017
----pack out---:MessagePack [_flag=6, _code=8, _messageId=11,reserved=0, _version=0, _statusCode=0, ack=0, _data={"msgId":"14bb3ed11a3e0018385cebdaf38d06af","receiptArray":[{"uid":"100060","readState":0,"readTime":0},{"uid":"100061","readState":0,"readTime":0},{"uid":"100062","readState":0,"readTime":0},{"uid":"100063","readState":0,"readTime":0},{"uid":"100020","readState":0,"readTime":0},{"uid":"100064","readState":0,"readTime":0},{"uid":"100021","readState":0,"readTime":0},{"uid":"100066","readState":0,"readTime":0},{"uid":"100022","readState":0,"readTime":0},{"uid":"100056","readState":0,"readTime":0},{"uid":"100012","readState":0,"readTime":0},{"uid":"100057","readState":0,"readTime":0},{"uid":"100013","readState":0,"readTime":0},{"uid":"100058","readState":0,"readTime":0},{"uid":"100014","readState":0,"readTime":0},{"uid":"100059","readState":0,"readTime":0},{"uid":"100015","readState":0,"readTime":0},{"uid":"100016","readState":0,"readTime":0},{"uid":"100017","readState":0,"readTime":0},{"uid":"100018","readState":0,"readTime":0},{"uid":"100019","readState":0,"readTime":0},{"uid":"100030","readState":0,"readTime":0},{"uid":"100031","readState":0,"readTime":0},{"uid":"100032","readState":0,"readTime":0},{"uid":"100033","readState":0,"readTime":0},{"uid":"100067","readState":0,"readTime":0},{"uid":"100023","readState":0,"readTime":0},{"uid":"100068","readState":0,"readTime":0},{"uid":"100024","readState":0,"readTime":0},{"uid":"100025","readState":0,"readTime":0},{"uid":"100026","readState":0,"readTime":0},{"uid":"100028","readState":0,"readTime":0},{"uid":"100029","readState":0,"readTime":0},{"uid":"100040","readState":0,"readTime":0},{"uid":"100041","readState":0,"readTime":0},{"uid":"100043","readState":0,"readTime":0},{"uid":"100000","readState":0,"readTime":0},{"uid":"100044","readState":0,"readTime":0},{"uid":"100034","readState":0,"readTime":0},{"uid":"100035","readState":0,"readTime":0},{"uid":"100036","readState":0,"readTime":0},{"uid":"100037","readState":0,"readTime":0},{"uid":"100038","readState":0,"readTime":0},{"uid":"100039","readState":0,"readTime":0},{"uid":"100050","readState":0,"readTime":0},{"uid":"100051","readState":0,"readTime":0},{"uid":"100053","readState":0,"readTime":0},{"uid":"100054","readState":0,"readTime":0},{"uid":"100010","readState":0,"readTime":0},{"uid":"100055","readState":0,"readTime":0},{"uid":"100011","readState":0,"readTime":0},{"uid":"100009","readState":0,"readTime":0},{"uid":"100","readState":1,"readTime":1497958125625},{"uid":"100001","readState":0,"readTime":0},{"uid":"100045","readState":0,"readTime":0},{"uid":"100002","readState":0,"readTime":0},{"uid":"100046","readState":0,"readTime":0},{"uid":"100047","readState":0,"readTime":0},{"uid":"100003","readState":0,"readTime":0},{"uid":"100048","readState":0,"readTime":0},{"uid":"100004","readState":0,"readTime":0},{"uid":"100005","readState":0,"readTime":0},{"uid":"100049","readState":0,"readTime":0},{"uid":"100006","readState":0,"readTime":0},{"uid":"100007","readState":0,"readTime":0},{"uid":"100008","readState":0,"readTime":0}]},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=8, _messageId=11,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]





发送消息 个人：
----pack in---:MessagePack [_flag=6, _code=1, _messageId=130,reserved=0, _version=0, _statusCode=0, ack=0, _data={"from":"99","to":"100","type":5,"content":"{\"text\":\"你18\"}","msgId":"a98d215b4ecadc5f01fcfbcd5b891d4e","device":"49E34C022874CB035EFB2052674DAFA9","spaceSize":5,"timestamp":1497953837727,"text":"你18"},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=1, _messageId=130,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 20, 2017 6:17:18 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:49, serverValue:94}] to 127.0.0.1:27017
2017-06-20 18:17:18,249 (MessageProcessor.java:65) INFO  com.shaozi.im.processors.MessageProcessor - build chatlog(ms)-:424
2017-06-20 18:17:18,328 (MessageProcessor.java:70) INFO  com.shaozi.im.processors.MessageProcessor - sendMessage(ms)-:71
2017-06-20 18:17:18,329 (ProcessHandlerManagerAOP.java:50) WARN  com.shaozi.im.aop.ProcessHandlerManagerAOP - flag:6,code:1,runs(ms):507--ChannelHandlerContext(ProcessCenterHandler#0, [id: 0x03172173, L:/10.3.21.117:1122 - R:/10.3.21.117:55630])
2017-06-20 18:17:18,329 (ProcessCenter.java:139) INFO  com.shaozi.im.protocol.processor.ProcessCenter - exec(ms):507;msgpack=MessagePack [_flag=6, _code=1, _messageId=130,reserved=0, _version=0, _statusCode=0, ack=0, _data={"messageCode":0,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"71181b84f90eb65844905e0d65c5d49f","from":"99","to":"100","type":5,"content":"{\"text\":\"你18\"}","timestamp":1497953837816,"device":"49E34C022874CB035EFB2052674DAFA9","fromIp":167974261,"fromPort":55630,"spaceSize":5,"shouldRecvNum":0,"oldMsgId":"a98d215b4ecadc5f01fcfbcd5b891d4e"},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=1, _messageId=29,reserved=0, _version=0, _statusCode=0, ack=0, _data={"msgId":"71181b84f90eb65844905e0d65c5d49f","oldMsgId":"a98d215b4ecadc5f01fcfbcd5b891d4e","timestamp":1497953837816,"type":46,"shouldRecvNum":1},resentCount=0]
----pack out---:MessagePack [_flag=6, _code=1, _messageId=9,reserved=0, _version=0, _statusCode=0, ack=0, _data={"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"sound":"im.wav","msgId":"71181b84f90eb65844905e0d65c5d49f","from":"99","to":"100","type":5,"content":"{\"text\":\"你18\"}","timestamp":1497953837816,"device":"49E34C022874CB035EFB2052674DAFA9","shouldRecvNum":1,"companyId":"10002","id":"5948f62ee8f8f20b9316670b"},resentCount=0]
----pack in---:MessagePack [_flag=6, _code=1, _messageId=29,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
----pack in---:MessagePack [_flag=6, _code=1, _messageId=9,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


创建通知流程

http://dev.t.api.shaozi.com/Stick/AddNotice
调用nc 的 nc/chatGroup/getMembers 取得群组的成员。

{"group_id":"4c9a0d2ab3767976284b98dafe1b1dda","title":"","content":"通知1720","type":2}

{"code":0,"msg":"请求成功。","data":{"stick_id":"594b8c00214b1a1f038b4568"},"devMsg":null,"trace":{"SQL":["demo_shaozi.getCollection(desk_stick) [ RunTime:0.0000s ]","demo_shaozi.getCollection(desk_stick_10002) [ RunTime:0.0000s ]","demo_shaozi.desk_stick_10002.findOne() [ RunTime:0.0002s ]","demo_shaozi.desk_stick_10002.insert({\"uid\":\"99\",\"title\":\"\",\"topic_md5\":\"\",\"group_id\":\"4c9a0d2ab3767976284b98dafe1b1dda\",\"content\":\"\\u901a\\u77e51720\",\"type\":2,\"priority\":0,\"stick\":1,\"status\":1,\"update_time\":1498123264049,\"insert_time\":1498123264049,\"end_time\":0,\"read_num\":0,\"relation\":[],\"actor_relation\":[\"99\"],\"group_user\":[99,100059,100046,100057,100051,100033,100045,100063,100,100067,100024,100002,100001,100000,100066,100044,100060,100056,100050,100062,100054,100065,100068,100061,100049,100055,100064,100022,100023,100020,100021,100019,100018,100027,100048,100058,100032,100052,100053,100047,100025,100029,100026,100031,100038,100028,100042,100040,100039,100037,100036,100035,100034,100014,100008,100007,100011,100017,100010,100013,100041,100012,100016,100015,100004,100003,100009,100006,100043,100069]}) [ RunTime:0.0003s ]"],"BASE":{"运行时间":"0.8961s ( Load:0.1205s Init:0.0230s Exec:0.7525s)","吞吐率":"1.12req\/s","内存开销":"3,044.88 kb","查询信息":"3 queries 1 writes ","文件加载":89,"缓存信息":"1 gets 0 writes "}}}

Thu Jun 22 17:21:04 CST 2017:----pack in---:MessagePack [_flag=6, _code=2, _messageId=71,reserved=0, _version=0, _statusCode=0, ack=0, _data={"from":"99","to":"4c9a0d2ab3767976284b98dafe1b1dda","type":49,"content":"{\"noticeId\":\"594b8c00214b1a1f038b4568\",\"noticeType\":1,\"text\":\"通知1720\"}","msgId":"05c8a6ad70f47f1aa7f9e1ad3e3e3a27","device":"49E34C022874CB035EFB2052674DAFA9","spaceSize":0,"timestamp":1498123264095,"noticeId":"594b8c00214b1a1f038b4568","noticeType":1,"text":"通知1720"},resentCount=0]
Thu Jun 22 17:21:04 CST 2017:----pack out---:MessagePack [_flag=6, _code=2, _messageId=71,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 22, 2017 5:21:04 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Closed connection [connectionId{localValue:11, serverValue:59}] to 127.0.0.1:27017 because it is past its maximum allowed idle time.
六月 22, 2017 5:21:04 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:12, serverValue:63}] to 127.0.0.1:27017
2017-06-22 17:21:04,367 (MessageProcessor.java:88) INFO  com.shaozi.im.processors.MessageProcessor - group build chatlog(ms)-:146
Thu Jun 22 17:21:04 CST 2017:----pack out---:MessagePack [_flag=6, _code=2, _messageId=8,reserved=0, _version=0, _statusCode=0, ack=0, _data={"msgId":"9cbdc147cf0848231733c01031e1a371","oldMsgId":"05c8a6ad70f47f1aa7f9e1ad3e3e3a27","timestamp":1498123264183,"type":46,"shouldRecvNum":69},resentCount=0]
2017-06-22 17:21:04,430 (MessageProcessor.java:93) INFO  com.shaozi.im.processors.MessageProcessor - sendMessageGroup(ms)-:56
2017-06-22 17:21:04,432 (ProcessCenter.java:139) INFO  com.shaozi.im.protocol.processor.ProcessCenter - exec(ms):215;msgpack=MessagePack [_flag=6, _code=2, _messageId=71,reserved=0, _version=0, _statusCode=0, ack=0, _data={"messageCode":0,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"9cbdc147cf0848231733c01031e1a371","from":"99","to":"4c9a0d2ab3767976284b98dafe1b1dda","type":49,"content":"{\"noticeId\":\"594b8c00214b1a1f038b4568\",\"noticeType\":1,\"text\":\"通知1720\"}","timestamp":1498123264183,"device":"49E34C022874CB035EFB2052674DAFA9","fromIp":167974261,"fromPort":62169,"spaceSize":0,"shouldRecvNum":0,"oldMsgId":"05c8a6ad70f47f1aa7f9e1ad3e3e3a27"},resentCount=0]
Thu Jun 22 17:21:04 CST 2017:----pack in---:MessagePack [_flag=6, _code=2, _messageId=8,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
2017-06-22 17:21:04,634 (PushDeviceManage.java:298) INFO  com.shaozi.im.business.push.PushDeviceManage - token为空:companyId,10002,userId:100,odb:OnlineDeviceBean [compId=10002, uid=100, apnsToken=null, platform=4, deviceId=A100005C51F04B, pushCount=0, isOff=true, pushType=1, environment=0]
Thu Jun 22 17:22:00 CST 2017:----pack in---:MessagePack [_flag=9, _code=1, _messageId=72,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
Thu Jun 22 17:22:00 CST 2017:----pack out---:MessagePack [_flag=9, _code=1, _messageId=72,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 22, 2017 5:22:05 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Closed connection [connectionId{localValue:12, serverValue:63}] to 127.0.0.1:27017 because it is past its maximum allowed idle time.


http://dev.t.api.shaozi.com/Stick/StickDetail?stick_id=594b8c00214b1a1f038b4568&type=2&start=0&limit=20

{"code":0,"msg":"请求成功。","data":{"comment_num":0,"read_num":0,"insert_time":1498123264049,"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","id":"594b8c00214b1a1f038b4568","content":"通知1720","confirmed":1,"actor_detail":[],"notice_confirmed":[],"notice_unconfirmed":[100059,100046,100057,100051,100033,100045,100063,100,100067,100024,100002,100001,100000,100066,100044,100060,100056,100050,100062,100054,100065,100068,100061,100049,100055,100064,100022,100023,100020,100021,100019,100018,100027,100048,100058,100032,100052,100053,100047,100025,100029,100026,100031,100038,100028,100042,100040,100039,100037,100036,100035,100034,100014,100008,100007,100011,100017,100010,100013,100041,100012,100016,100015,100004,100003,100009,100006,100043,100069],"comment":[]},"devMsg":null,"trace":{"SQL":["demo_shaozi.getCollection(desk_stick) [ RunTime:0.0000s ]","demo_shaozi.getCollection(desk_stick_10002) [ RunTime:0.0000s ]","demo_shaozi.desk_stick_10002.findOne() [ RunTime:0.0003s ]","demo_shaozi.desk_stick_10002.find({\"_id\":{\"$id\":\"594b8c00214b1a1f038b4568\"}}).limit(1) [ RunTime:0.0000s ]","SHOW COLUMNS FROM `desk_stick_notice` [ RunTime:0.0013s ]","SELECT * FROM `desk_stick_notice` WHERE `stick_id` IN ('594b8c00214b1a1f038b4568') AND `company_id` = 10002  [ RunTime:0.0008s ]","demo_shaozi.desk_stick_10002.findOne() [ RunTime:0.0004s ]","demo_shaozi.desk_stick_10002.update({\"_id\":{\"$id\":\"594b8c00214b1a1f038b4568\"}},{\"$inc\":{\"read_num\":1}}) [ RunTime:0.0005s ]","SHOW COLUMNS FROM `desk_stick_comment` [ RunTime:0.0014s ]","SELECT * FROM `desk_stick_comment` WHERE `stick_id` = '594b8c00214b1a1f038b4568' AND `company_id` = 10002 ORDER BY insert_time desc LIMIT 0,20   [ RunTime:0.0009s ]"],"BASE":{"运行时间":"1.0621s ( Load:0.2745s Init:0.0284s Exec:0.7593s)","吞吐率":"0.94req\/s","内存开销":"3,573.06 kb","查询信息":"9 queries 1 writes ","文件加载":94,"缓存信息":"1 gets 0 writes "}}}

http://dev.t.api.shaozi.com/Stick/TopThree?group_id=4c9a0d2ab3767976284b98dafe1b1dda


{"code":0,"msg":"请求成功。","data":[{"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"通知1720","type":2,"insert_time":1498123264049,"end_time":0,"read_num":1,"id":"594b8c00214b1a1f038b4568","actor_num":0,"confirmed":1,"total_num":69,"comment_num":0},{"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"通知3","type":2,"insert_time":1498122728200,"end_time":0,"read_num":1,"id":"594b89e8214b1a1f038b4567","actor_num":0,"confirmed":1,"total_num":69,"comment_num":0},{"uid":"99","title":"222","topic_md5":"","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":{"anonymouse":0,"max_selected":1,"end_time":1498206120000,"options":{"1":"1","2":"2"}},"type":3,"status":1,"insert_time":1498121688585,"end_time":1498206120000,"read_num":0,"id":"594b85d8214b1a89028b4569","voted_num":0,"voted":0,"total_num":69,"comment_num":0}],"devMsg":null,"trace":{"SQL":["demo_shaozi.getCollection(desk_stick) [ RunTime:0.0000s ]","demo_shaozi.getCollection(desk_stick_10002) [ RunTime:0.0000s ]","demo_shaozi.desk_stick_10002.findOne() [ RunTime:0.0003s ]","demo_shaozi.desk_stick_10002.find({\"group_id\":\"4c9a0d2ab3767976284b98dafe1b1dda\",\"stick\":1,\"relation\":{\"$nin\":[\"99\"]},\"insert_time\":{\"$gt\":0}}).sort({\"insert_time\":-1}).limit(3) [ RunTime:0.0000s ]","SHOW COLUMNS FROM `desk_stick_vote` [ RunTime:0.0051s ]","SELECT * FROM `desk_stick_vote` WHERE `stick_id` IN ('594b8c00214b1a1f038b4568','594b89e8214b1a1f038b4567','594b85d8214b1a89028b4569') AND `company_id` = 10002  [ RunTime:0.0005s ]"],"BASE":{"运行时间":"1.1226s ( Load:0.2458s Init:0.0458s Exec:0.8310s)","吞吐率":"0.89req\/s","内存开销":"3,327.86 kb","查询信息":"6 queries 0 writes ","文件加载":94,"缓存信息":"1 gets 0 writes "}}}


http://dev.t.api.shaozi.com/Stick/Stick?group_id=4c9a0d2ab3767976284b98dafe1b1dda&type=2&start=0&limit=20


{"code":0,"msg":"请求成功。","data":{"total":23,"my_count":13,"my_relation_count":13,"data":[{"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"通知1720","type":2,"insert_time":1498123264049,"end_time":0,"read_num":0,"id":"594b8c00214b1a1f038b4568","actor_num":0,"confirmed":1,"total_num":69,"comment_num":0},{"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"通知3","type":2,"insert_time":1498122728200,"end_time":0,"read_num":1,"id":"594b89e8214b1a1f038b4567","actor_num":0,"confirmed":1,"total_num":69,"comment_num":0},{"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"通知3","type":2,"insert_time":1498121584005,"end_time":0,"read_num":0,"id":"594b856f214b1aec028b4567","actor_num":0,"confirmed":1,"total_num":69,"comment_num":0},{"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"通知3","type":2,"insert_time":1498121334393,"end_time":0,"read_num":0,"id":"594b8476214b1a8c028b4568","actor_num":0,"confirmed":1,"total_num":69,"comment_num":0},{"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"通知3","type":2,"insert_time":1498121332792,"end_time":0,"read_num":0,"id":"594b8474214b1a81028b4568","actor_num":0,"confirmed":1,"total_num":69,"comment_num":0},{"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"通知3","type":2,"insert_time":1498121328298,"end_time":0,"read_num":0,"id":"594b8470214b1a89028b4568","actor_num":0,"confirmed":1,"total_num":69,"comment_num":0},{"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"通知3","type":2,"insert_time":1498121054640,"end_time":0,"read_num":0,"id":"594b835e214b1a8c028b4567","actor_num":0,"confirmed":1,"total_num":69,"comment_num":0},{"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"通知3","type":2,"insert_time":1498120871174,"end_time":0,"read_num":0,"id":"594b82a7214b1a81028b4567","actor_num":0,"confirmed":1,"total_num":69,"comment_num":0},{"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"通知3","type":2,"insert_time":1498119773284,"end_time":0,"read_num":0,"id":"594b7e5d214b1a89028b4567","actor_num":0,"confirmed":1,"total_num":69,"comment_num":0},{"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"通知2","type":2,"insert_time":1498015569155,"end_time":0,"read_num":0,"id":"5949e751490b493c058b4567","actor_num":0,"confirmed":1,"total_num":0,"comment_num":0},{"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"通知2","type":2,"insert_time":1498013287699,"end_time":0,"read_num":0,"id":"5949de67490b49bc048b4567","actor_num":0,"confirmed":1,"total_num":0,"comment_num":0},{"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"通知1","type":2,"insert_time":1498013161254,"end_time":0,"read_num":0,"id":"5949dde9490b49a5048b4567","actor_num":0,"confirmed":1,"total_num":0,"comment_num":0},{"uid":"99","group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"通知1","type":2,"insert_time":1498013157009,"end_time":0,"read_num":0,"id":"5949dde5490b49a6048b4567","actor_num":0,"confirmed":1,"total_num":0,"comment_num":0},{"uid":100002,"group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"明天晚上九点聚餐","type":2,"insert_time":1496383852719,"end_time":0,"read_num":67,"id":"5931016ce3900f0e11f6e521","actor_num":21,"confirmed":0,"total_num":69,"comment_num":0},{"uid":100016,"group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"111","type":2,"insert_time":1495847258957,"end_time":0,"read_num":69,"id":"5928d15ae3900f3a0df6e515","actor_num":19,"confirmed":0,"total_num":69,"comment_num":0},{"uid":100066,"group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"明天晚上八点聚餐。","type":2,"insert_time":1495636912803,"end_time":0,"read_num":58,"comment_num":1,"id":"59259bb0e3900f1f0bf6e515","actor_num":19,"confirmed":0,"total_num":69},{"uid":100056,"group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"111","type":2,"insert_time":1495620256020,"end_time":0,"read_num":40,"id":"59255aa0e3900f1f0bf6e514","actor_num":9,"confirmed":0,"total_num":69,"comment_num":0},{"uid":100049,"group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"123","type":2,"insert_time":1494830168264,"end_time":0,"read_num":44,"id":"59194c58e3900f827e33ae64","actor_num":10,"confirmed":0,"total_num":10,"comment_num":0},{"uid":100056,"group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"明天放假","type":2,"insert_time":1494320218168,"end_time":0,"read_num":49,"id":"5911845ae3900fad0433ae65","actor_num":14,"confirmed":0,"total_num":14,"comment_num":0},{"uid":100006,"group_id":"4c9a0d2ab3767976284b98dafe1b1dda","content":"测试","type":2,"insert_time":1494224691876,"end_time":0,"read_num":43,"comment_num":1,"id":"59100f33e3900fd51b33ae64","actor_num":14,"confirmed":0,"total_num":14}]},"devMsg":null,"trace":{"SQL":["demo_shaozi.getCollection(desk_stick) [ RunTime:0.0000s ]","demo_shaozi.getCollection(desk_stick_10002) [ RunTime:0.0000s ]","demo_shaozi.desk_stick_10002.findOne() [ RunTime:0.0005s ]","demo_shaozi.desk_stick_10002.find({\"group_id\":\"4c9a0d2ab3767976284b98dafe1b1dda\",\"type\":2}).count() [ RunTime:0.0006s ]","demo_shaozi.desk_stick_10002.findOne() [ RunTime:0.0004s ]","demo_shaozi.desk_stick_10002.find({\"group_id\":\"4c9a0d2ab3767976284b98dafe1b1dda\",\"type\":2}).sort({\"insert_time\":-1}).limit(20) [ RunTime:0.0000s ]","SHOW COLUMNS FROM `desk_stick_vote` [ RunTime:0.0125s ]","SELECT * FROM `desk_stick_vote` WHERE `stick_id` IN ('594b8c00214b1a1f038b4568','594b89e8214b1a1f038b4567','594b856f214b1aec028b4567','594b8476214b1a8c028b4568','594b8474214b1a81028b4568','594b8470214b1a89028b4568','594b835e214b1a8c028b4567','594b82a7214b1a81028b4567','594b7e5d214b1a89028b4567','5949e751490b493c058b4567','5949de67490b49bc048b4567','5949dde9490b49a5048b4567','5949dde5490b49a6048b4567','5931016ce3900f0e11f6e521','5928d15ae3900f3a0df6e515','59259bb0e3900f1f0bf6e515','59255aa0e3900f1f0bf6e514','59194c58e3900f827e33ae64','5911845ae3900fad0433ae65','59100f33e3900fd51b33ae64') AND `company_id` = 10002  [ RunTime:0.0010s ]","demo_shaozi.desk_stick_10002.findOne() [ RunTime:0.0004s ]","demo_shaozi.desk_stick_10002.find({\"group_id\":\"4c9a0d2ab3767976284b98dafe1b1dda\",\"type\":2,\"uid\":\"99\"}).count() [ RunTime:0.0005s ]","demo_shaozi.desk_stick_10002.findOne() [ RunTime:0.0003s ]","demo_shaozi.desk_stick_10002.find({\"group_id\":\"4c9a0d2ab3767976284b98dafe1b1dda\",\"type\":2,\"actor_relation\":{\"$in\":[\"99\"]}}).count() [ RunTime:0.0004s ]"],"BASE":{"运行时间":"1.1058s ( Load:0.2747s Init:0.0252s Exec:0.8059s)","吞吐率":"0.90req\/s","内存开销":"3,370.84 kb","查询信息":"12 queries 0 writes ","文件加载":93,"缓存信息":"1 gets 0 writes "}}}


用户进来登陆通知表情

2017-06-22 21:11:49,903 (ProcessCenter.java:139) INFO  com.shaozi.im.protocol.processor.ProcessCenter - exec(ms):307;msgpack=MessagePack [_flag=11, _code=2, _messageId=94,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":1496824323778},resentCount=0]
Thu Jun 22 21:11:49 CST 2017:----pack out---:MessagePack [_flag=11, _code=2, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=0, _data={"insert":[],"update":[],"delete":[],"maxIdentity":1496824323778},resentCount=0]
2017-06-22 21:11:49,919 (ProcessCenter.java:139) INFO  com.shaozi.im.protocol.processor.ProcessCenter - exec(ms):233;msgpack=MessagePack [_flag=6, _code=18, _messageId=97,reserved=0, _version=0, _statusCode=0, ack=0, _data={"tos":["24"]},resentCount=0]
Thu Jun 22 21:11:49 CST 2017:----pack out---:MessagePack [_flag=6, _code=18, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=0, _data=[{"to":"24","count":0}],resentCount=0]
Thu Jun 22 21:11:49 CST 2017:----pack in---:MessagePack [_flag=11, _code=2, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Thu Jun 22 21:11:49 CST 2017:----pack in---:MessagePack [_flag=6, _code=18, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Thu Jun 22 21:11:49 CST 2017:----pack in---:MessagePack [_flag=6, _code=13, _messageId=99,reserved=0, _version=0, _statusCode=0, ack=0, _data={"length":1,"queryId":"24","updateId":0},resentCount=0]
Thu Jun 22 21:11:49 CST 2017:----pack out---:MessagePack [_flag=6, _code=13, _messageId=99,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Thu Jun 22 21:11:50 CST 2017:----pack out---:MessagePack [_flag=6, _code=13, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=0, _data={"datas":[{"messageCode":3,"receiptNum":69,"lastReceiptTime":0,"readState":1,"msgId":"fa8532ea0174833525aa9175315189c6","from":"100025","to":"24","type":5,"content":"{\"text\":\"测试\",\"style\":\"\",\"act\":\"0\"}","timestamp":1493796383071,"shouldRecvNum":69}],"updateId":1498137109972},resentCount=0]
Thu Jun 22 21:11:50 CST 2017:----pack in---:MessagePack [_flag=6, _code=13, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Thu Jun 22 21:11:50 CST 2017:----pack out---:MessagePack [_flag=6, _code=17, _messageId=7,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[],"revokes":[],"datas":[{"messageCode":2,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"9cbdc147cf0848231733c01031e1a371","from":"99","to":"4c9a0d2ab3767976284b98dafe1b1dda","type":49,"content":"{\"noticeId\":\"594b8c00214b1a1f038b4568\",\"noticeType\":1,\"text\":\"通知1720\"}","timestamp":1498123264183,"shouldRecvNum":69},{"messageCode":2,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"090544fe95c68aec8842a6dbe7879b1a","from":"99","to":"4c9a0d2ab3767976284b98dafe1b1dda","type":49,"content":"{\"noticeId\":\"594b89e8214b1a1f038b4567\",\"noticeType\":1,\"text\":\"通知3\"}","timestamp":1498122728561,"shouldRecvNum":69}],"updateId":1498123264183},resentCount=0]
Thu Jun 22 21:11:50 CST 2017:----pack in---:MessagePack [_flag=6, _code=17, _messageId=7,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Thu Jun 22 21:12:07 CST 2017:----pack in---:MessagePack [_flag=6, _code=20, _messageId=100,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"content":"{\"receiptMsgId\":\"9568c934d79b90f967c92385eb4f808a\",\"receiptTo\":\"100\",\"receiptType\":2}","device":"A100005C51F04B","from":"100","msgId":"86bca7f4859847f0a9c0fb755e439724","readState":1,"to":"100029"},{"content":"{\"receiptMsgId\":\"82b5797566657c2edbad250c6157e630\",\"receiptTo\":\"100\",\"receiptType\":2}","device":"A100005C51F04B","from":"100","msgId":"43e5ef3ea0b04c13a1dfca0a4def87d5","readState":1,"to":"100029"},{"content":"{\"receiptMsgId\":\"7a0050186222ac66e8f90f31919c045d\",\"receiptTo\":\"100\",\"receiptType\":2}","device":"A100005C51F04B","from":"100","msgId":"e0b28b94f61a4b2bbb214155359a7fe9","readState":1,"to":"100027"},{"content":"{\"receiptMsgId\":\"090544fe95c68aec8842a6dbe7879b1a\",\"receiptTo\":\"100\",\"receiptType\":2}","device":"A100005C51F04B","from":"100","msgId":"858b90ba26294f1eab592f8220e88bc7","readState":1,"to":"99"},{"content":"{\"receiptMsgId\":\"9cbdc147cf0848231733c01031e1a371\",\"receiptTo\":\"100\",\"receiptType\":2}","device":"A100005C51F04B","from":"100","msgId":"b0836e546f8340a482527f9b8de64e0c","readState":1,"to":"99"}]},resentCount=0]
Thu Jun 22 21:12:07 CST 2017:----pack out---:MessagePack [_flag=6, _code=20, _messageId=100,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
2017-06-22 21:12:07,920 (ProcessCenter.java:139) INFO  com.shaozi.im.protocol.processor.ProcessCenter - exec(ms):264;msgpack=MessagePack [_flag=6, _code=20, _messageId=100,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"content":"{\"receiptMsgId\":\"9568c934d79b90f967c92385eb4f808a\",\"receiptTo\":\"100\",\"receiptType\":2}","device":"A100005C51F04B","from":"100","msgId":"86bca7f4859847f0a9c0fb755e439724","readState":1,"to":"100029"},{"content":"{\"receiptMsgId\":\"82b5797566657c2edbad250c6157e630\",\"receiptTo\":\"100\",\"receiptType\":2}","device":"A100005C51F04B","from":"100","msgId":"43e5ef3ea0b04c13a1dfca0a4def87d5","readState":1,"to":"100029"},{"content":"{\"receiptMsgId\":\"7a0050186222ac66e8f90f31919c045d\",\"receiptTo\":\"100\",\"receiptType\":2}","device":"A100005C51F04B","from":"100","msgId":"e0b28b94f61a4b2bbb214155359a7fe9","readState":1,"to":"100027"},{"content":"{\"receiptMsgId\":\"090544fe95c68aec8842a6dbe7879b1a\",\"receiptTo\":\"100\",\"receiptType\":2}","device":"A100005C51F04B","from":"100","msgId":"858b90ba26294f1eab592f8220e88bc7","readState":1,"to":"99"},{"content":"{\"receiptMsgId\":\"9cbdc147cf0848231733c01031e1a371\",\"receiptTo\":\"100\",\"receiptType\":2}","device":"A100005C51F04B","from":"100","msgId":"b0836e546f8340a482527f9b8de64e0c","readState":1,"to":"99"}]},resentCount=0]
Thu Jun 22 21:12:08 CST 2017:----pack out---:MessagePack [_flag=6, _code=20, _messageId=11,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"messageCode":0,"receiptNum":1,"lastReceiptTime":0,"readState":1,"msgId":"090544fe95c68aec8842a6dbe7879b1a","from":"100","to":"99","type":0,"content":"{\"receiptMsgId\":\"090544fe95c68aec8842a6dbe7879b1a\",\"receiptNum\":1,\"receiptTo\":\"100\",\"receiptType\":2,\"readState\":1}","timestamp":1498137127640,"device":"A100005C51F04B","fromIp":167974322,"fromPort":43324,"shouldRecvNum":0,"oldMsgId":"858b90ba26294f1eab592f8220e88bc7"},{"messageCode":0,"receiptNum":1,"lastReceiptTime":0,"readState":1,"msgId":"9cbdc147cf0848231733c01031e1a371","from":"100","to":"99","type":0,"content":"{\"receiptMsgId\":\"9cbdc147cf0848231733c01031e1a371\",\"receiptNum\":1,\"receiptTo\":\"100\",\"receiptType\":2,\"readState\":1}","timestamp":1498137127640,"device":"A100005C51F04B","fromIp":167974322,"fromPort":43324,"shouldRecvNum":0,"oldMsgId":"b0836e546f8340a482527f9b8de64e0c"}],"updateId":1498137127640},resentCount=0]
Thu Jun 22 21:12:08 CST 2017:----pack in---:MessagePack [_flag=6, _code=20, _messageId=11,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Thu Jun 22 21:12:37 CST 2017:----pack in---:MessagePack [_flag=9, _code=1, _messageId=101,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
Thu Jun 22 21:12:37 CST 2017:----pack out---:MessagePack [_flag=9, _code=1, _messageId=101,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]



创建群组
在线的直接发送创建群组，然后发送推送群组消息。不在线的不发。
Thu Jun 22 21:35:18 CST 2017:----pack in---:MessagePack [_flag=11, _code=1, _messageId=343,reserved=0, _version=0, _statusCode=0, ack=0, _data={"groupId":"","operate":"create","data":["100","100044","99"],"gName":"尚文清,陈璐荷,石玉兰"},resentCount=0]
Thu Jun 22 21:35:18 CST 2017:----pack out---:MessagePack [_flag=11, _code=1, _messageId=343,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 22, 2017 9:35:18 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:47, serverValue:111}] to 127.0.0.1:27017
2017-06-22 21:35:18,352 (ChatGroupManage.java:89) INFO  com.shaozi.im.business.manage.ChatGroupManage - not get chat group,compId=10002,gid=6e7c0c7313aeb0f628b561e14731dc7f
Thu Jun 22 21:35:18 CST 2017:----pack out---:MessagePack [_flag=11, _code=1, _messageId=13,reserved=0, _version=0, _statusCode=0, ack=0, _data={"gName":"尚文清,陈璐荷,石玉兰","gNPinyin":"SHANGWENQING,CHENLUHE,DANYULAN,SHANGWENQING,CHENLUHE,SHIYULAN,","gNPYHead":"SWQ,CLH,SYL,SWQ,CLH,DYL,","groupId":"6e7c0c7313aeb0f628b561e14731dc7f","creator":"99","groupType":1,"lastUpdateTime":1498138518673,"createTime":1498138518352,"members":["99","100","100044"]},resentCount=0]
Thu Jun 22 21:35:18 CST 2017:----pack in---:MessagePack [_flag=11, _code=1, _messageId=13,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Thu Jun 22 21:35:18 CST 2017:----pack out---:MessagePack [_flag=11, _code=1, _messageId=13,reserved=0, _version=0, _statusCode=0, ack=0, _data={"gName":"尚文清,陈璐荷,石玉兰","gNPinyin":"SHANGWENQING,CHENLUHE,DANYULAN,SHANGWENQING,CHENLUHE,SHIYULAN,","gNPYHead":"SWQ,CLH,SYL,SWQ,CLH,DYL,","groupId":"6e7c0c7313aeb0f628b561e14731dc7f","creator":"99","groupType":1,"lastUpdateTime":1498138518673,"createTime":1498138518352,"members":["99","100","100044"]},resentCount=0]
2017-06-22 21:35:18,697 (ProcessCenter.java:139) INFO  com.shaozi.im.protocol.processor.ProcessCenter - exec(ms):410;msgpack=MessagePack [_flag=11, _code=1, _messageId=343,reserved=0, _version=0, _statusCode=0, ack=0, _data={"groupId":"","operate":"create","data":["100","100044","99"],"gName":"尚文清,陈璐荷,石玉兰"},resentCount=0]
Thu Jun 22 21:35:18 CST 2017:----pack out---:MessagePack [_flag=6, _code=2, _messageId=10,reserved=0, _version=0, _statusCode=0, ack=0, _data={"messageCode":2,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"0a31ccb1af55fdb93068066ebe68c03f","from":"99","to":"6e7c0c7313aeb0f628b561e14731dc7f","type":201,"content":"{\"members\":[\"100\",\"100044\",\"99\"],\"creator\":\"99\",\"gName\":\"尚文清,陈璐荷,石玉兰\",\"groupType\":1}","timestamp":1498138518691,"device":"system control message","shouldRecvNum":0,"oldMsgId":"083bbc6ca2fa68a275b34b1a120506fc"},resentCount=0]
Thu Jun 22 21:35:18 CST 2017:----pack out---:MessagePack [_flag=6, _code=2, _messageId=10,reserved=0, _version=0, _statusCode=0, ack=0, _data={"messageCode":2,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"0a31ccb1af55fdb93068066ebe68c03f","from":"99","to":"6e7c0c7313aeb0f628b561e14731dc7f","type":201,"content":"{\"members\":[\"100\",\"100044\",\"99\"],\"creator\":\"99\",\"gName\":\"尚文清,陈璐荷,石玉兰\",\"groupType\":1}","timestamp":1498138518691,"device":"system control message","shouldRecvNum":0,"oldMsgId":"083bbc6ca2fa68a275b34b1a120506fc"},resentCount=0]


推送通知

Thu Jun 22 21:54:23 CST 2017:----pack in---:MessagePack [_flag=6, _code=2, _messageId=365,reserved=0, _version=0, _statusCode=0, ack=0, _data={"from":"99","to":"6e7c0c7313aeb0f628b561e14731dc7f","type":49,"content":"{\"noticeId\":\"594bcc0e214b1adb038b4567\",\"noticeType\":1,\"text\":\"通知2154\"}","msgId":"bfc127189c6941ae580996c1feac5134","device":"49E34C022874CB035EFB2052674DAFA9","spaceSize":0,"timestamp":1498139663037,"noticeId":"594bcc0e214b1adb038b4567","noticeType":1,"text":"通知2154"},resentCount=0]
Thu Jun 22 21:54:23 CST 2017:----pack out---:MessagePack [_flag=6, _code=2, _messageId=365,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 22, 2017 9:54:51 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:50, serverValue:121}] to 127.0.0.1:27017
六月 22, 2017 9:56:04 下午 com.mongodb.diagnostics.logging.JULLogger log
Thu Jun 22 21:56:55 CST 2017:----pack out---:MessagePack [_flag=6, _code=2, _messageId=16,reserved=0, _version=0, _statusCode=0, ack=0, _data={"msgId":"21f358baccb6a5dea977118e968ff95a","oldMsgId":"bfc127189c6941ae580996c1feac5134","timestamp":1498139663161,"type":46,"shouldRecvNum":2},resentCount=0]
Thu Jun 22 21:56:55 CST 2017:----pack in---:MessagePack [_flag=6, _code=2, _messageId=16,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 22, 2017 9:57:35 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:51, serverValue:122}] to 127.0.0.1:27017
六月 22, 2017 9:59:04 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Closed connection [connectionId{localValue:51, serverValue:122}] to 127.0.0.1:27017 because it is past its maximum allowed idle time.
Thu Jun 22 21:59:08 CST 2017:----pack out---:MessagePack [_flag=6, _code=2, _messageId=11,reserved=0, _version=0, _statusCode=0, ack=0, _data={"messageCode":2,"receiptNum":0,"lastReceiptTime":0,"readState":0,"sound":"im.wav","msgId":"21f358baccb6a5dea977118e968ff95a","from":"99","to":"6e7c0c7313aeb0f628b561e14731dc7f","type":49,"content":"{\"noticeId\":\"594bcc0e214b1adb038b4567\",\"noticeType\":1,\"text\":\"通知2154\"}","timestamp":1498139663161,"device":"49E34C022874CB035EFB2052674DAFA9","shouldRecvNum":2,"companyId":"10002","id":"594bcc2be8f8f240910905bd"},resentCount=0]
Thu Jun 22 21:59:08 CST 2017:----pack in---:MessagePack [_flag=6, _code=2, _messageId=11,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 22, 2017 10:00:00 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:52, serverValue:123}] to 127.0.0.1:27017
2017-06-22 22:00:29,335 (MessageProcessor.java:93) INFO  com.shaozi.im.processors.MessageProcessor - sendMessageGroup(ms)-:314874
2017-06-22 22:00:29,337 (ProcessHandlerManagerAOP.java:50) WARN  com.shaozi.im.aop.ProcessHandlerManagerAOP - flag:6,code:2,runs(ms):366145--ChannelHandlerContext(ProcessCenterHandler#0, [id: 0x03a6af09, L:/10.3.21.117:1122 - R:/10.3.21.117:62169])
2017-06-22 22:00:29,339 (ProcessCenter.java:139) INFO  com.shaozi.im.protocol.processor.ProcessCenter - exec(ms):366147;msgpack=MessagePack [_flag=6, _code=2, _messageId=365,reserved=0, _version=0, _statusCode=0, ack=0, _data={"messageCode":0,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"21f358baccb6a5dea977118e968ff95a","from":"99","to":"6e7c0c7313aeb0f628b561e14731dc7f","type":49,"content":"{\"noticeId\":\"594bcc0e214b1adb038b4567\",\"noticeType\":1,\"text\":\"通知2154\"}","timestamp":1498139663161,"device":"49E34C022874CB035EFB2052674DAFA9","fromIp":167974261,"fromPort":62169,"spaceSize":0,"shouldRecvNum":0,"oldMsgId":"bfc127189c6941ae580996c1feac5134"},resentCount=0]

点击进来通知 已经读
Thu Jun 22 22:19:32 CST 2017:----pack in---:MessagePack [_flag=6, _code=20, _messageId=283,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"content":"{\"receiptMsgId\":\"0a31ccb1af55fdb93068066ebe68c03f\",\"receiptTo\":\"100\",\"receiptType\":2}","device":"A100005C51F04B","from":"100","msgId":"09597d90a5894c2788becc5767d3ccd7","readState":1,"to":"99"},{"content":"{\"receiptMsgId\":\"21f358baccb6a5dea977118e968ff95a\",\"receiptTo\":\"100\",\"receiptType\":2}","device":"A100005C51F04B","from":"100","msgId":"65ef31f5129f48c7833cfe79969f0a6b","readState":1,"to":"99"}]},resentCount=0]
Thu Jun 22 22:19:32 CST 2017:----pack out---:MessagePack [_flag=6, _code=20, _messageId=283,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Thu Jun 22 22:19:32 CST 2017:----pack out---:MessagePack [_flag=6, _code=20, _messageId=39,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"messageCode":0,"receiptNum":1,"lastReceiptTime":0,"readState":1,"msgId":"0a31ccb1af55fdb93068066ebe68c03f","from":"100","to":"99","type":0,"content":"{\"receiptMsgId\":\"0a31ccb1af55fdb93068066ebe68c03f\",\"receiptNum\":1,\"receiptTo\":\"100\",\"receiptType\":2,\"readState\":1}","timestamp":1498141172267,"device":"A100005C51F04B","fromIp":167974322,"fromPort":43825,"shouldRecvNum":0,"oldMsgId":"09597d90a5894c2788becc5767d3ccd7"},{"messageCode":0,"receiptNum":1,"lastReceiptTime":0,"readState":1,"msgId":"21f358baccb6a5dea977118e968ff95a","from":"100","to":"99","type":0,"content":"{\"receiptMsgId\":\"21f358baccb6a5dea977118e968ff95a\",\"receiptNum\":1,\"receiptTo\":\"100\",\"receiptType\":2,\"readState\":1}","timestamp":1498141172267,"device":"A100005C51F04B","fromIp":167974322,"fromPort":43825,"shouldRecvNum":0,"oldMsgId":"65ef31f5129f48c7833cfe79969f0a6b"}],"updateId":1498141172267},resentCount=0]
Thu Jun 22 22:19:32 CST 2017:----pack in---:MessagePack [_flag=6, _code=20, _messageId=39,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

确认通知
Thu Jun 22 22:20:45 CST 2017:----pack in---:MessagePack [_flag=6, _code=2, _messageId=286,reserved=0, _version=0, _statusCode=0, ack=0, _data={"content":"{\"msgId\":\"ed4d14baf13b4bd6acc6b9437202efba\",\"noticeId\":\"594bcc0e214b1adb038b4567\",\"noticeType\":3,\"title\":\"通知2154\"}","device":"A100005C51F04B","from":"100","msgId":"ed4d14baf13b4bd6acc6b9437202efba","spaceSize":141,"timestamp":1498141245493,"to":"6e7c0c7313aeb0f628b561e14731dc7f","type":49},resentCount=0]
Thu Jun 22 22:20:45 CST 2017:----pack out---:MessagePack [_flag=6, _code=2, _messageId=286,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
2017-06-22 22:20:48,914 (NoticeSureManage.java:74) INFO  com.shaozi.im.business.manage.NoticeSureManage - compId:10002,groupId:6e7c0c7313aeb0f628b561e14731dc7f,noticeId:594bcc0e214b1adb038b4567,type:1
2017-06-22 22:20:49,223 (NoticeSureManage.java:78) INFO  com.shaozi.im.business.manage.NoticeSureManage - noticeSure:null
2017-06-22 22:20:49,247 (MessageProcessor.java:88) INFO  com.shaozi.im.processors.MessageProcessor - group build chatlog(ms)-:3394
Thu Jun 22 22:20:52 CST 2017:----pack out---:MessagePack [_flag=6, _code=2, _messageId=8,reserved=0, _version=0, _statusCode=0, ack=0, _data={"msgId":"c633bd504f5ac91e5686c5623846c7ac","oldMsgId":"ed4d14baf13b4bd6acc6b9437202efba","timestamp":1498141245845,"type":46,"shouldRecvNum":2},resentCount=0]
Thu Jun 22 22:20:52 CST 2017:----pack in---:MessagePack [_flag=6, _code=2, _messageId=8,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
2017-06-22 22:20:53,767 (MessageProcessor.java:93) INFO  com.shaozi.im.processors.MessageProcessor - sendMessageGroup(ms)-:4520
2017-06-22 22:20:53,768 (ProcessHandlerManagerAOP.java:50) WARN  com.shaozi.im.aop.ProcessHandlerManagerAOP - flag:6,code:2,runs(ms):7916--ChannelHandlerContext(ProcessCenterHandler#0, [id: 0xf4500c9e, L:/10.3.21.117:1122 - R:/10.3.21.178:43825])
Thu Jun 22 22:20:53 CST 2017:----pack out---:MessagePack [_flag=6, _code=2, _messageId=40,reserved=0, _version=0, _statusCode=0, ack=0, _data={"messageCode":2,"receiptNum":0,"lastReceiptTime":0,"readState":0,"sound":"im.wav","msgId":"c633bd504f5ac91e5686c5623846c7ac","from":"100","to":"6e7c0c7313aeb0f628b561e14731dc7f","type":49,"content":"{\"msgId\":\"ed4d14baf13b4bd6acc6b9437202efba\",\"noticeId\":\"594bcc0e214b1adb038b4567\",\"noticeType\":3,\"title\":\"通知2154\"}","timestamp":1498141245845,"device":"A100005C51F04B","shouldRecvNum":2,"companyId":"10002","id":"594bd241e8f8f240910905c1"},resentCount=0]
2017-06-22 22:20:53,771 (ProcessCenter.java:139) INFO  com.shaozi.im.protocol.processor.ProcessCenter - exec(ms):7921;msgpack=MessagePack [_flag=6, _code=2, _messageId=286,reserved=0, _version=0, _statusCode=0, ack=0, _data={"messageCode":0,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"c633bd504f5ac91e5686c5623846c7ac","from":"100","to":"6e7c0c7313aeb0f628b561e14731dc7f","type":49,"content":"{\"msgId\":\"ed4d14baf13b4bd6acc6b9437202efba\",\"noticeId\":\"594bcc0e214b1adb038b4567\",\"noticeType\":3,\"title\":\"通知2154\"}","timestamp":1498141245845,"device":"A100005C51F04B","fromIp":167974322,"fromPort":43825,"spaceSize":141,"shouldRecvNum":0,"oldMsgId":"ed4d14baf13b4bd6acc6b9437202efba"},resentCount=0]
Thu Jun 22 22:20:53 CST 2017:----pack in---:MessagePack [_flag=6, _code=2, _messageId=40,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

Thu Jun 22 22:20:53 CST 2017:----pack in---:MessagePack [_flag=6, _code=2, _messageId=40,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Thu Jun 22 22:21:22 CST 2017:----pack in---:MessagePack [_flag=9, _code=1, _messageId=287,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
Thu Jun 22 22:21:22 CST 2017:----pack out---:MessagePack [_flag=9, _code=1, _messageId=287,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Thu Jun 22 22:21:49 CST 2017:----pack in---:MessagePack [_flag=9, _code=1, _messageId=385,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
Thu Jun 22 22:21:49 CST 2017:----pack out---:MessagePack [_flag=9, _code=1, _messageId=385,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Thu Jun 22 22:21:54 CST 2017:----pack in---:MessagePack [_flag=9, _code=1, _messageId=288,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
Thu Jun 22 22:21:54 CST 2017:----pack out---:MessagePack [_flag=9, _code=1, _messageId=288,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 22, 2017 10:22:04 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Closed connection [connectionId{localValue:66, serverValue:139}] to 127.0.0.1:27017 because it is past its maximum allowed idle time.
Thu Jun 22 22:22:45 CST 2017:----pack in---:MessagePack [_flag=9, _code=1, _messageId=386,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
Thu Jun 22 22:22:45 CST 2017:----pack out---:MessagePack [_flag=9, _code=1, _messageId=386,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Thu Jun 22 22:22:45 CST 2017:----pack in---:MessagePack [_flag=9, _code=1, _messageId=289,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
Thu Jun 22 22:22:45 CST 2017:----pack out---:MessagePack [_flag=9, _code=1, _messageId=289,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Thu Jun 22 22:23:31 CST 2017:----pack in---:MessagePack [_flag=9, _code=1, _messageId=290,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
Thu Jun 22 22:23:31 CST 2017:----pack out---:MessagePack [_flag=9, _code=1, _messageId=290,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Thu Jun 22 22:23:39 CST 2017:----pack in---:MessagePack [_flag=6, _code=20, _messageId=387,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"from":"99","to":"100","content":"{\"receiptMsgId\":\"c633bd504f5ac91e5686c5623846c7ac\",\"receiptTo\":\"6e7c0c7313aeb0f628b561e14731dc7f\",\"receiptType\":2}","msgId":"962c35be123e32ac68822971fef83b04","device":"49E34C022874CB035EFB2052674DAFA9"}]},resentCount=0]
Thu Jun 22 22:23:39 CST 2017:----pack out---:MessagePack [_flag=6, _code=20, _messageId=387,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
六月 22, 2017 10:23:39 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:68, serverValue:151}] to 127.0.0.1:27017
Thu Jun 22 22:23:39 CST 2017:----pack out---:MessagePack [_flag=6, _code=20, _messageId=9,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"messageCode":0,"receiptNum":1,"lastReceiptTime":0,"readState":1,"msgId":"c633bd504f5ac91e5686c5623846c7ac","from":"99","to":"100","type":0,"content":"{\"receiptMsgId\":\"c633bd504f5ac91e5686c5623846c7ac\",\"receiptNum\":1,\"receiptTo\":\"6e7c0c7313aeb0f628b561e14731dc7f\",\"receiptType\":2,\"readState\":1}","timestamp":1498141419100,"device":"49E34C022874CB035EFB2052674DAFA9","fromIp":167974261,"fromPort":62169,"shouldRecvNum":0,"oldMsgId":"962c35be123e32ac68822971fef83b04"}],"updateId":1498141419100},resentCount=0]
Thu Jun 22 22:23:39 CST 2017:----pack in---:MessagePack [_flag=6, _code=20, _messageId=9,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Thu Jun 22 22:24:32 CST 2017:----pack in---:MessagePack [_flag=9, _code=1, _messageId=291,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
Thu Jun 22 22:24:32 CST 2017:----pack out---:MessagePack [_flag=9, _code=1, _messageId=291,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]



创建审批推送
六月 23, 2017 11:31:37 上午 com.mongodb.diagnostics.logging.JULLogger log
信息: Closed connection [connectionId{localValue:120, serverValue:275}] to 127.0.0.1:27017 because it is past its maximum allowed idle time.
Fri Jun 23 11:31:43 CST 2017:----pack out---:MessagePack [_flag=2, _code=3, _messageId=13,reserved=0, _version=0, _statusCode=0, ack=0, _data={"sourceType":6500,"moduleType":6500,"fromUserId":"1","toUserId":"99","extra":"[{\"tab\":3,\"id\":\"238\"}]","notifyType":1,"isRead":0},resentCount=0]
Fri Jun 23 11:31:43 CST 2017:----pack in---:MessagePack [_flag=2, _code=3, _messageId=13,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Fri Jun 23 11:31:43 CST 2017:----pack out---:MessagePack [_flag=2, _code=3, _messageId=14,reserved=0, _version=0, _statusCode=0, ack=0, _data={"sourceType":6500,"moduleType":6500,"fromUserId":"1","toUserId":"100","extra":"[{\"tab\":3,\"id\":\"238\"}]","notifyType":1,"isRead":0},resentCount=0]
Fri Jun 23 11:31:43 CST 2017:----pack in---:MessagePack [_flag=9, _code=1, _messageId=431,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
Fri Jun 23 11:31:44 CST 2017:----pack out---:MessagePack [_flag=2, _code=1, _messageId=14,reserved=0, _version=0, _statusCode=0, ack=0, _data={"id":"594c8ba0e8f8f2772e465cc3","secretaryId":"594c8ba0e8f8f2772e465cc3","sourceType":6504,"moduleType":6500,"fromUserId":"1","toUserId":"99","title":"审批提醒","content":"尚文清发起了测试审批，请及时处理。","extra":"{\"id\":238,\"triggerUserId\":\"100\"}","updateTime":1498188703912,"insertTime":1498188703912,"notifyType":1,"isRead":0,"sound":"im.wav"},resentCount=0]


[{"cron":true,"cronExpression":"30 5 0 * * ?","jobOperatorType":0,"maxRetryTimes":0,"needFeedback":false,"priority":100,"relyOnPrevCycle":true,"repeatCount":0,"repeatable":false,"replaceOnExist":true,"taskGroupName":"Nc_Attendance_Sign_Rule_GroupName","taskId":"Nc_Attendance_Sign_Rule_Id","taskTrackerNodeGroup":"shaozi_yun_steven_nc_trade_TaskTracker"}, {"cron":true,"cronExpression":"30 15 5 * * ?","jobOperatorType":0,"maxRetryTimes":0,"needFeedback":false,"priority":100,"relyOnPrevCycle":true,"repeatCount":0,"repeatable":false,"replaceOnExist":true,"taskGroupName":"Nc_Crm_Sale_Open_See_Recover_GroupName","taskId":"Nc_Crm_Sale_Open_See_Recover_Id","taskTrackerNodeGroup":"shaozi_yun_steven_nc_trade_TaskTracker"}, {"cron":true,"cronExpression":"30 15 5 * * ?","jobOperatorType":0,"maxRetryTimes":0,"needFeedback":false,"priority":100,"relyOnPrevCycle":true,"repeatCount":0,"repeatable":false,"replaceOnExist":true,"taskGroupName":"Nc_Crm_Sale_Quite_Open_See_Recover_GroupName","taskId":"Nc_Crm_Sale_Quite_Open_See_Recover_Id","taskTrackerNodeGroup":"shaozi_yun_steven_nc_trade_TaskTracker"}]

{Nc_Crm_Sale_Quite_Open_See_Recover_GroupName,Nc_Crm_Sale_Quite_Open_See_Recover_Id=com.shaozi.job.task.base.ClassMehtodBean@5b1dd206, Nc_Crm_Sale_Open_See_Recover_GroupName,Nc_Crm_Sale_Open_See_Recover_Id=com.shaozi.job.task.base.ClassMehtodBean@3ea4dcc5, Nc_Attendance_Sign_Rule_GroupName,Nc_Attendance_Sign_Rule_Id_Send_=com.shaozi.job.task.base.ClassMehtodBean@73611fbb, Nc_Report_GroupName,Nc_Report_Id_Send_=com.shaozi.job.task.base.ClassMehtodBean@3d0f2154, Nc_Test_GroupName,Nc_Test_Id=com.shaozi.job.task.base.ClassMehtodBean@8374911, Nc_Attendance_Sign_Rule_GroupName,Nc_Attendance_Sign_Rule_Id=com.shaozi.job.task.base.ClassMehtodBean@106dee26}
----
com.shaozi.nc.job.biz.CrmSaleQuiteOpenSeeJob@18213a65


审批规则
{"isDebug":0,"companyId":"10002","action_type":1,"dataTime":1498208658117,"rule":{"biz":[{"userIds":[99,100],"extra":"[{\"tab\":3,\"id\":\"239\"}]","type":6500}],"push":{"sourceId":239,"atTime":0,"sourceType":19001,"levelType":1,"title":"","pushRegex":"","userId":100,"content":""}}}
api.badge
[BadgeBean [userIds=[99, 100], type=6500, extra=[{"tab":3,"id":"239"}]]]


{"isDebug":0,"companyId":"10002","action_type":1,"dataTime":1498208658091,"rule":{"biz":{"followUserIds":[99],"formName":"测试","id":239,"userId":100},"push":{"sourceId":239,"atTime":0,"sourceType":6504,"levelType":1,"title":"","pushRegex":"","userId":100,"content":""}}}
com.push.secretary

[{"type":6500,"sourceType":19001,"pushType":3,"notifyType":1,"triggerUserId":"100","fromUserId":"1","users":[{"userId":"99","userType":0,"isRead":0,"isDel":0},{"userId":"100","userType":0,"isRead":0,"isDel":0}],"extra":"[{\"tab\":3,\"id\":\"239\"}]","isDebug":0,"createTime":1498209351551,"mqTime":1498208658390,"triggerTime":1498208658117,"sound":"im.wav","uuid":"31493aa11e2535b5c77139802680f596","companyId":"10002"}]




{attendanceRuleJob=com.shaozi.nc.job.biz.AttendanceRuleJob@2f7e2481, crmSaleOpenSeeRecoverJob=com.shaozi.nc.job.biz.CrmSaleOpenSeeRecoverJob@2f19ab6, crmSaleQuiteOpenSeeJob=com.shaozi.nc.job.biz.CrmSaleQuiteOpenSeeJob@4d5aeea7, reportJob=com.shaozi.nc.job.biz.ReportJob@6f8b1902, testJob=com.shaozi.nc.job.biz.TestJob@2c914aa3}


#没推 重新推
2017-06-26 17:16:32,623 (AndroidDeviceClient.java:81) INFO  com.shaozi.im.lib.push.xiaomi.AndroidDeviceClient - appMasterSecret:W2SVma1kFezmBgmbUbFgsA==,token:uGB+Wj62Wgb+AnHWrXVy8Gq3GoiilVL/ucL5YplUCUg=,sender:com.xiaomi.xmpush.server.Sender@41598f40
Mon Jun 26 17:17:28 CST 2017:----pack in---:MessagePack [_flag=9, _code=1, _messageId=47,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
Mon Jun 26 17:17:28 CST 2017:----pack out---:MessagePack [_flag=9, _code=1, _messageId=47,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]


信息: Closed connection [connectionId{localValue:2, serverValue:236}] to 127.0.0.1:27017 because it is past its maximum allowed idle time.
2017-06-26 17:40:24,696  INFO QueryTranslatorFactoryInitiator:47 - HHH000397: Using ASTQueryTranslatorFactory
Hibernate:
    select
        attendance0_.id as id1_1_,
        attendance0_.company_id as company_2_1_,
        attendance0_.is_delete as is_delet3_1_,
        attendance0_.punsh_in_time as punsh_in4_1_,
        attendance0_.punsh_out_time as punsh_ou5_1_,
        attendance0_.rule_id as rule_id6_1_
    from
        desk_attendance_level attendance0_
    where
        attendance0_.is_delete=0
        and attendance0_.company_id=10002
2017-06-26 17:40:25,588  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:in,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@c35e3b4;id=1;companyId=10002punsh_in_time=09:00, punsh_out_time=17:00, isDelete=0, ruleId=1,punchTime:09:00,type:1,startAt:1498470085587
2017-06-26 17:40:25,598  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,600  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@c35e3b4;id=1;companyId=10002punsh_in_time=09:00, punsh_out_time=17:00, isDelete=0, ruleId=1,punchTime:17:00,type:2,startAt:1498470085600
2017-06-26 17:40:25,610  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,612  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:in,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@73350aeb;id=2;companyId=10002punsh_in_time=09:00, punsh_out_time=19:00, isDelete=0, ruleId=2,punchTime:09:00,type:1,startAt:1498470085612
2017-06-26 17:40:25,622  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,624  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@73350aeb;id=2;companyId=10002punsh_in_time=09:00, punsh_out_time=19:00, isDelete=0, ruleId=2,punchTime:19:00,type:2,startAt:1498475400624
2017-06-26 17:40:25,633  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,636  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:in,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@76e407b1;id=3;companyId=10002punsh_in_time=09:00, punsh_out_time=18:00, isDelete=0, ruleId=3,punchTime:09:00,type:1,startAt:1498470085635
2017-06-26 17:40:25,646  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,648  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@76e407b1;id=3;companyId=10002punsh_in_time=09:00, punsh_out_time=18:00, isDelete=0, ruleId=3,punchTime:18:00,type:2,startAt:1498471800647
2017-06-26 17:40:25,660  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,661  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:in,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@7086e001;id=4;companyId=10002punsh_in_time=09:00, punsh_out_time=18:00, isDelete=0, ruleId=4,punchTime:09:00,type:1,startAt:1498470085661
2017-06-26 17:40:25,673  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,675  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@7086e001;id=4;companyId=10002punsh_in_time=09:00, punsh_out_time=18:00, isDelete=0, ruleId=4,punchTime:18:00,type:2,startAt:1498471800675
2017-06-26 17:40:25,684  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,686  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:in,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@497ba045;id=5;companyId=10002punsh_in_time=09:00, punsh_out_time=18:00, isDelete=0, ruleId=5,punchTime:09:00,type:1,startAt:1498470085686
2017-06-26 17:40:25,697  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,699  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@497ba045;id=5;companyId=10002punsh_in_time=09:00, punsh_out_time=18:00, isDelete=0, ruleId=5,punchTime:18:00,type:2,startAt:1498471800699
2017-06-26 17:40:25,708  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,710  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:in,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@12c289d3;id=6;companyId=10002punsh_in_time=10:00, punsh_out_time=11:00, isDelete=0, ruleId=5,punchTime:10:00,type:1,startAt:1498470085710
2017-06-26 17:40:25,721  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,723  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@12c289d3;id=6;companyId=10002punsh_in_time=10:00, punsh_out_time=11:00, isDelete=0, ruleId=5,punchTime:11:00,type:2,startAt:1498470085723
2017-06-26 17:40:25,734  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,736  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:in,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@44cdddb5;id=7;companyId=10002punsh_in_time=12:00, punsh_out_time=14:00, isDelete=0, ruleId=5,punchTime:12:00,type:1,startAt:1498470085736
2017-06-26 17:40:25,745  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,747  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@44cdddb5;id=7;companyId=10002punsh_in_time=12:00, punsh_out_time=14:00, isDelete=0, ruleId=5,punchTime:14:00,type:2,startAt:1498470085747
2017-06-26 17:40:25,756  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,758  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:in,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@30cabc5;id=8;companyId=10002punsh_in_time=09:00, punsh_out_time=18:00, isDelete=0, ruleId=6,punchTime:09:00,type:1,startAt:1498470085758
2017-06-26 17:40:25,768  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,770  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@30cabc5;id=8;companyId=10002punsh_in_time=09:00, punsh_out_time=18:00, isDelete=0, ruleId=6,punchTime:18:00,type:2,startAt:1498471800769
2017-06-26 17:40:25,780  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,782  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:in,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@17614a69;id=9;companyId=10002punsh_in_time=09:00, punsh_out_time=17:30, isDelete=0, ruleId=6,punchTime:09:00,type:1,startAt:1498470085782
2017-06-26 17:40:25,793  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,794  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@17614a69;id=9;companyId=10002punsh_in_time=09:00, punsh_out_time=17:30, isDelete=0, ruleId=6,punchTime:17:30,type:2,startAt:1498470085794
2017-06-26 17:40:25,804  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,806  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:in,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@11ebc547;id=10;companyId=10002punsh_in_time=09:00, punsh_out_time=20:00, isDelete=0, ruleId=7,punchTime:09:00,type:1,startAt:1498470085806
2017-06-26 17:40:25,816  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,817  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@11ebc547;id=10;companyId=10002punsh_in_time=09:00, punsh_out_time=20:00, isDelete=0, ruleId=7,punchTime:20:00,type:2,startAt:1498479000817
2017-06-26 17:40:25,832  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,834  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:in,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@3b6182ba;id=11;companyId=10002punsh_in_time=21:00, punsh_out_time=23:00, isDelete=0, ruleId=7,punchTime:21:00,type:1,startAt:1498481400834
2017-06-26 17:40:25,845  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,847  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@3b6182ba;id=11;companyId=10002punsh_in_time=21:00, punsh_out_time=23:00, isDelete=0, ruleId=7,punchTime:23:00,type:2,startAt:1498489800846
2017-06-26 17:40:25,857  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,859  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:in,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@5dd55490;id=12;companyId=10002punsh_in_time=09:00, punsh_out_time=18:00, isDelete=0, ruleId=8,punchTime:09:00,type:1,startAt:1498470085859
2017-06-26 17:40:25,868  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,870  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@5dd55490;id=12;companyId=10002punsh_in_time=09:00, punsh_out_time=18:00, isDelete=0, ruleId=8,punchTime:18:00,type:2,startAt:1498471800869
2017-06-26 17:40:25,882  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,884  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:in,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@407a7f41;id=13;companyId=10002punsh_in_time=09:30, punsh_out_time=18:00, isDelete=0, ruleId=8,punchTime:09:30,type:1,startAt:1498470085884
2017-06-26 17:40:25,892  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,893  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@407a7f41;id=13;companyId=10002punsh_in_time=09:30, punsh_out_time=18:00, isDelete=0, ruleId=8,punchTime:18:00,type:2,startAt:1498471800893
2017-06-26 17:40:25,903  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,905  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:in,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@f744bf4;id=14;companyId=10002punsh_in_time=10:00, punsh_out_time=18:00, isDelete=0, ruleId=8,punchTime:10:00,type:1,startAt:1498470085905
2017-06-26 17:40:25,915  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,918  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@f744bf4;id=14;companyId=10002punsh_in_time=10:00, punsh_out_time=18:00, isDelete=0, ruleId=8,punchTime:18:00,type:2,startAt:1498471800918
2017-06-26 17:40:25,934  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:40:25,935  INFO AttendanceSignRuleManage:84 - companyId=10002;level size=14
2017-06-26 17:45:08,494  INFO AttendanceSignQuartzJob:99 - companyId=10002;levelId=1;job trigger,isObserver:false,punchTime:17:00
Hibernate:
    select
        attendance0_.id as id1_0_,
        attendance0_.company_id as company_2_0_,
        attendance0_.is_appeal_expire as is_appea3_0_,
        attendance0_.is_delete as is_delet4_0_,
        attendance0_.json_rule as json_rul5_0_,
        attendance0_.level_id as level_id6_0_,
        attendance0_.rule_handle_time as rule_han7_0_,
        attendance0_.start_handle_time as start_ha8_0_,
        attendance0_.status as status9_0_,
        attendance0_.status_type as status_10_0_,
        attendance0_.sys_insert_time as sys_ins11_0_,
        attendance0_.type as type12_0_,
        attendance0_.uid as uid13_0_
    from
        desk_attendance attendance0_
    where
        attendance0_.status=0
        and attendance0_.level_id=1
        and attendance0_.sys_insert_time>=1498406400
        and attendance0_.sys_insert_time<=1498492799
        and attendance0_.type=2
        and attendance0_.company_id=10002
        and attendance0_.is_delete=0

        2017-06-26 17:49:17,942  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:13,type:1
        2017-06-26 17:49:17,974  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:9,type:2
        2017-06-26 17:49:18,012  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:4,type:1
        2017-06-26 17:49:18,048  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:1,type:1
        2017-06-26 17:49:18,094  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:3,type:1
        2017-06-26 17:49:18,110  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:6,type:2
        2017-06-26 17:49:18,111  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:12,type:1
        2017-06-26 17:49:18,140  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:14,type:1
        2017-06-26 17:49:18,150  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:10,type:1
        2017-06-26 17:49:18,150  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:6,type:1
        2017-06-26 17:49:18,150  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:9,type:1
        2017-06-26 17:49:18,159  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:5,type:1
        2017-06-26 17:49:18,161  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:8,type:1
        2017-06-26 17:49:18,179  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:7,type:2
        2017-06-26 17:49:18,183  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:2,type:1
        2017-06-26 17:49:18,185  WARN AttendanceSignQuartzJob:104 - 考勤定时任务执行, 查询 考情列表数据 查询今天未打卡的数据 为空 则不执行提醒任务，companyId:10002,levelId:1,type:2
        Hibernate:
            select

            2017-06-26 17:50:18,610  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:50:18,611  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@4472b360;id=13;companyId=10002punsh_in_time=09:30, punsh_out_time=18:00, isDelete=0, ruleId=8,punchTime:18:00,type:2,startAt:1498471800611
2017-06-26 17:50:18,620  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:50:18,620  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:in,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@68338178;id=14;companyId=10002punsh_in_time=10:00, punsh_out_time=18:00, isDelete=0, ruleId=8,punchTime:10:00,type:1,startAt:1498470678620
2017-06-26 17:50:18,628  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:50:18,629  INFO AttendanceSignRuleManage:75 - scheduleByAttendanceLevel to addAttendanceSignJob companyId:10002,io:out,vo:com.shaozi.nc.data.hibVO.AttendanceLevelVO@68338178;id=14;companyId=10002punsh_in_time=10:00, punsh_out_time=18:00, isDelete=0, ruleId=8,punchTime:18:00,type:2,startAt:1498471800629
2017-06-26 17:50:18,638  INFO JobClientAdd:30 - {"success":true}
2017-06-26 17:50:18,639  INFO AttendanceSignRuleManage:84 - companyId=10002;level size=14






Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=6, _code=18, _messageId=710,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=11, _code=2, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=0, _data={"insert":[],"update":[],"delete":[],"maxIdentity":1498138518673},resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=3, _code=2, _messageId=711,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=3, _code=2, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":0},resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=1, _code=8, _messageId=712,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=1, _code=8, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=6, _code=18, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=0, _data=[{"to":"24","count":0}],resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=1, _code=1, _messageId=1,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=11, _code=2, _messageId=713,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":1498138518673},resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=3, _code=2, _messageId=714,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":0},resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=6, _code=17, _messageId=715,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":1498466943105},resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=11, _code=2, _messageId=713,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=3, _code=2, _messageId=714,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=3, _code=2, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=0, _data={"updateId":0},resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=6, _code=17, _messageId=715,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=6, _code=18, _messageId=716,reserved=0, _version=0, _statusCode=0, ack=0, _data={"tos":["24"]},resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=1, _code=8, _messageId=717,reserved=0, _version=0, _statusCode=0, ack=0, _data={"deviceId":"A100005C51F04B","platform":4,"pushType":1,"token":"uGB+Wj62Wgb+AnHWrXVy8Gq3GoiilVL/ucL5YplUCUg=","uid":"100"},resentCount=0]
六月 26, 2017 5:59:20 下午 com.mongodb.diagnostics.logging.JULLogger log
信息: Opened connection [connectionId{localValue:72, serverValue:243}] to 127.0.0.1:27017
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=11, _code=2, _messageId=2,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=3, _code=2, _messageId=3,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=1, _code=8, _messageId=4,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=6, _code=18, _messageId=5,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=6, _code=18, _messageId=716,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=11, _code=2, _messageId=7,reserved=0, _version=0, _statusCode=0, ack=0, _data={"insert":[],"update":[],"delete":[],"maxIdentity":1498138518673},resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=1, _code=8, _messageId=717,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=1, _code=8, _messageId=8,reserved=0, _version=0, _statusCode=0, ack=0, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=6, _code=18, _messageId=9,reserved=0, _version=0, _statusCode=0, ack=0, _data=[{"to":"24","count":0}],resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=3, _code=2, _messageId=6,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=6, _code=13, _messageId=718,reserved=0, _version=0, _statusCode=0, ack=0, _data={"length":1,"queryId":"24","updateId":0},resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=11, _code=2, _messageId=7,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=1, _code=8, _messageId=8,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=6, _code=13, _messageId=718,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=6, _code=18, _messageId=9,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=6, _code=13, _messageId=719,reserved=0, _version=0, _statusCode=0, ack=0, _data={"length":1,"queryId":"24","updateId":0},resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=6, _code=13, _messageId=719,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack out---:MessagePack [_flag=6, _code=17, _messageId=10,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"receiptMsgId":"6349984deb0961cb2825cc340866e4d7","receiptNum":1,"receiptTo":"99","receiptType":2,"readState":1},{"receiptMsgId":"3b90a19393f7b1edfaae3d114363db7e","receiptNum":1,"receiptTo":"99","receiptType":2,"readState":1},{"receiptMsgId":"c1554d53ea0f6fd65407eb123506e05f","receiptNum":1,"receiptTo":"99","receiptType":2,"readState":1},{"receiptMsgId":"1b664e49d15e581d4a66bef1921e5408","receiptNum":1,"receiptTo":"99","receiptType":2,"readState":1}],"revokes":[],"datas":[{"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"f8a9ed96122cba6bf02105c4cc70ffd4","from":"99","to":"100","type":5,"content":"{\"text\":\"44\"}","timestamp":1498467777516,"shouldRecvNum":1},{"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"5d0ba6d9f98436e823834b2554428794","from":"99","to":"100","type":5,"content":"{\"text\":\"22\"}","timestamp":1498467775572,"shouldRecvNum":1}],"updateId":1498467777516},resentCount=0]
Mon Jun 26 17:59:20 CST 2017:----pack in---:MessagePack [_flag=6, _code=17, _messageId=10,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:21 CST 2017:----pack out---:MessagePack [_flag=6, _code=13, _messageId=11,reserved=0, _version=0, _statusCode=0, ack=0, _data={"datas":[{"messageCode":3,"receiptNum":69,"lastReceiptTime":0,"readState":1,"msgId":"fa8532ea0174833525aa9175315189c6","from":"100025","to":"24","type":5,"content":"{\"text\":\"测试\",\"style\":\"\",\"act\":\"0\"}","timestamp":1493796383071,"shouldRecvNum":69}],"updateId":1498471160698},resentCount=0]
Mon Jun 26 17:59:21 CST 2017:----pack in---:MessagePack [_flag=6, _code=13, _messageId=11,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:21 CST 2017:----pack out---:MessagePack [_flag=6, _code=13, _messageId=12,reserved=0, _version=0, _statusCode=0, ack=0, _data={"datas":[{"messageCode":3,"receiptNum":69,"lastReceiptTime":0,"readState":1,"msgId":"fa8532ea0174833525aa9175315189c6","from":"100025","to":"24","type":5,"content":"{\"text\":\"测试\",\"style\":\"\",\"act\":\"0\"}","timestamp":1493796383071,"shouldRecvNum":69}],"updateId":1498471160733},resentCount=0]
Mon Jun 26 17:59:21 CST 2017:----pack in---:MessagePack [_flag=6, _code=13, _messageId=12,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]
Mon Jun 26 17:59:21 CST 2017:----pack out---:MessagePack [_flag=6, _code=17, _messageId=13,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"receiptMsgId":"6349984deb0961cb2825cc340866e4d7","receiptNum":1,"receiptTo":"99","receiptType":2,"readState":1},{"receiptMsgId":"3b90a19393f7b1edfaae3d114363db7e","receiptNum":1,"receiptTo":"99","receiptType":2,"readState":1},{"receiptMsgId":"c1554d53ea0f6fd65407eb123506e05f","receiptNum":1,"receiptTo":"99","receiptType":2,"readState":1},{"receiptMsgId":"1b664e49d15e581d4a66bef1921e5408","receiptNum":1,"receiptTo":"99","receiptType":2,"readState":1}],"revokes":[],"datas":[{"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"f8a9ed96122cba6bf02105c4cc70ffd4","from":"99","to":"100","type":5,"content":"{\"text\":\"44\"}","timestamp":1498467777516,"shouldRecvNum":1},{"messageCode":1,"receiptNum":0,"lastReceiptTime":0,"readState":0,"msgId":"5d0ba6d9f98436e823834b2554428794","from":"99","to":"100","type":5,"content":"{\"text\":\"22\"}","timestamp":1498467775572,"shouldRecvNum":1}],"updateId":1498467777516},resentCount=0]
Mon Jun 26 17:59:21 CST 2017:----pack in---:MessagePack [_flag=6, _code=17, _messageId=13,reserved=0, _version=0, _statusCode=0, ack=1, _data=null,resentCount=0]

NC:
2017-06-26 17:01:54,253  INFO App:57 - Started App in 3.734 seconds (JVM running for 4.277)
2017-06-26 17:36:03,969  INFO ChatLogUpdateIgnoreBean:72 - notMatchCount:10000
2017-06-26 18:10:29,829  INFO ChatLogUpdateIgnoreBean:72 - notMatchCount:20000




回执
{"receipts":[{"from":"99","to":"100","content":"{\"receiptMsgId\":\"c6088d2008d6cd9eba7357981c40cd09\",\"receiptTo\":\"99\",\"receiptType\":1}","msgId":"d0274df75b8a2465fba97179732bc06b","device":"49E34C022874CB035EFB2052674DAFA9"}]}

Query: { "msgId" : { "$in" : [ "c6088d2008d6cd9eba7357981c40cd09"]} , "companyId" : "10002"}, Fields: { "messageCode" : 1 , "timestamp" : 1}, Sort: { "timestamp" : -1}

Query: { "msgId" : "c6088d2008d6cd9eba7357981c40cd09" , "companyId" : "10002"}, Fields: { "from" : 1 , "to" : 1}, Sort: null

Query: { "msgId" : { "$in" : [ "c6088d2008d6cd9eba7357981c40cd09"]} , "receiptArray" : { "$elemMatch" : { "uid" : "99" , "readState" : { "$ne" : 1}}} , "companyId" : "10002"}, Fields: null, Sort: null
{ "$set" : { "receiptArray.$.readState" : 1 , "receiptArray.$.readTime" : 1498718294670 , "lastReceiptTime" : 1498718294670} , "$inc" : { "receiptNum" : 1}}

im-ChatLogUpdateIgnore-10002 {"companyId":"10002","receipterId":"99","queryId":"100","msgCode":1,"msgTime":1498718256404,"collectionName":"im_ChatLog_002"}

Query: { "msgId" : { "$in" : [ "c6088d2008d6cd9eba7357981c40cd09"]} , "companyId" : "10002"}, Fields: { "receiptNum" : 1 , "msgId" : 1}, Sort: null

MessagePack [_flag=6, _code=20, _messageId=7,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"messageCode":0,"receiptNum":0,"lastReceiptTime":0,"readState":1,"msgId":"c6088d2008d6cd9eba7357981c40cd09","from":"99","to":"100","type":0,"content":"{\"receiptMsgId\":\"c6088d2008d6cd9eba7357981c40cd09\",\"receiptTo\":\"99\",\"receiptType\":1}","timestamp":1498718294670,"device":"49E34C022874CB035EFB2052674DAFA9","shouldRecvNum":0}],"updateId":1498718294670},resentCount=0]


MessagePack [_flag=6, _code=20, _messageId=0,reserved=0, _version=0, _statusCode=0, ack=0, _data={"receipts":[{"messageCode":0,"receiptNum":1,"lastReceiptTime":0,"readState":1,"msgId":"c6088d2008d6cd9eba7357981c40cd09","from":"99","to":"100","type":0,"content":"{\"receiptMsgId\":\"c6088d2008d6cd9eba7357981c40cd09\",\"receiptNum\":1,\"receiptTo\":\"99\",\"receiptType\":1,\"readState\":1}","timestamp":1498718294670,"device":"49E34C022874CB035EFB2052674DAFA9","fromIp":167974261,"fromPort":55731,"shouldRecvNum":0,"oldMsgId":"d0274df75b8a2465fba97179732bc06b"}],"updateId":1498718294670},resentCount=0]

 lrange im-ChatLogUpdateIgnore-10002 0 1

{"companyId":"10002","receipterId":"100","queryId":"99","msgCode":1,"msgTime":1498729744144,"collectionName":"im_ChatLog_002"}
 100_from_99_to_100
 Query: { "timestamp" : { "$lte" : 1498729744144} , "from" : "99" , "to" : "100" , "receiptArray" : { "$elemMatch" : { "uid" : "100" , "readState" : 0}}}, Fields: null, Sort: null
 { "$set" : { "receiptArray.$.readState" : 2}}
