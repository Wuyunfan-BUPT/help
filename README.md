## Test Cases Info


|Total|Success|Failure|Error|Skipped|
|-----|-------|-------|-----|-------|
|78|9|23|42|4|


### :x: Failed Case Detail

#### Name:  [com.alibaba.nacos.config.ConfigNormalTest.testPublishAndAddOneListener]<https://github.com/nacos-group/nacos-e2e/tree/main/java/nacos-2X/src/test/java/com/alibaba/nacos/config/ConfigNormalTest.java#L94?target="_blank"> Time: 0.303s

<details>
<summary>Exception Detail</summary>


**Exception**
org.opentest4j.AssertionFailedError: publishConfig check fail ==> expected: <true> but was: <false>
	at com.alibaba.nacos.config.ConfigNormalTest.testPublishAndAddOneListener(ConfigNormalTest.java:94)

**System out info**
2023-06-15 04:55:58 INFO  [c.a.n.n.SubscribeClusterTest  #setUp               :  39] Running test=Optional[public void com.alibaba.nacos.naming.SubscribeClusterTest.testSubscribeDelete() throws java.lang.Exception], serviceName=nacos.HMlwA.AhWDS.com
2023-06-15 04:55:58 INFO  [c.a.n.c.naming                #registerService     : 121] [REGISTER-SERVICE] public registering service nacos.HMlwA.AhWDS.com with instance Instance{instanceId='null', ip='127.0.0.1', port=8848, weight=1.0, healthy=true, enabled=true, ephemeral=true, clusterName='c1', serviceName='null', metadata={}}
2023-06-15 04:55:58 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = InstanceRequest{headers={app=unknown}, requestId='null'}, retryTimes = 1, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:58 INFO  [c.a.n.c.r.c.g.GrpcClient      #ateNewManagedChannel: 182] grpc client connection server:127.0.0.1 ip,serverPort:9848,grpcTslConfig:{"sslProvider":"","enableTls":false,"mutualAuthEnable":false,"trustAll":false}
2023-06-15 04:55:58 INFO  [c.a.n.c.r.c.g.GrpcClient      #ateNewManagedChannel: 182] grpc client connection server:127.0.0.1 ip,serverPort:9848,grpcTslConfig:{"sslProvider":"","enableTls":false,"mutualAuthEnable":false,"trustAll":false}
2023-06-15 04:55:58 ERROR [c.a.n.c.r.c.g.GrpcClient      #printIfErrorEnabled : 102] Server check fail, please check server 127.0.0.1 ,port 9848 is available , error ={}
java.util.concurrent.ExecutionException: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.getDoneValue(AbstractFuture.java:566)
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.get(AbstractFuture.java:445)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.serverCheck(GrpcClient.java:218)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.connectToServer(GrpcClient.java:329)
	at com.alibaba.nacos.common.remote.client.RpcClient.reconnect(RpcClient.java:502)
	at com.alibaba.nacos.common.remote.client.RpcClient.lambda$start$2(RpcClient.java:343)
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
	at java.util.concurrent.FutureTask.run(FutureTask.java:266)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.access$201(ScheduledThreadPoolExecutor.java:180)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:293)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)
Caused by: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.io.grpc.Status.asRuntimeException(Status.java:539)
	at com.alibaba.nacos.shaded.io.grpc.stub.ClientCalls$UnaryStreamToFuture.onClose(ClientCalls.java:544)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener$3.run(DelayedClientCall.java:471)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.delayOrExecute(DelayedClientCall.java:435)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.onClose(DelayedClientCall.java:468)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.closeObserver(ClientCallImpl.java:563)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.access$300(ClientCallImpl.java:70)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInternal(ClientCallImpl.java:744)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInContext(ClientCallImpl.java:723)
	at com.alibaba.nacos.shaded.io.grpc.internal.ContextRunnable.run(ContextRunnable.java:37)
	at com.alibaba.nacos.shaded.io.grpc.internal.SerializingExecutor.run(SerializingExecutor.java:133)
	... 3 common frames omitted
Caused by: com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.AbstractChannel$AnnotatedConnectException: Connection refused: /127.0.0.1:9848
Caused by: java.net.ConnectException: Connection refused
	at sun.nio.ch.SocketChannelImpl.checkConnect(Native Method)
	at sun.nio.ch.SocketChannelImpl.finishConnect(SocketChannelImpl.java:716)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.socket.nio.NioSocketChannel.doFinishConnect(NioSocketChannel.java:337)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.AbstractNioChannel$AbstractNioUnsafe.finishConnect(AbstractNioChannel.java:334)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKey(NioEventLoop.java:710)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeysOptimized(NioEventLoop.java:658)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeys(NioEventLoop.java:584)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.run(NioEventLoop.java:496)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.SingleThreadEventExecutor$4.run(SingleThreadEventExecutor.java:997)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.internal.ThreadExecutorMap$2.run(ThreadExecutorMap.java:74)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.FastThreadLocalRunnable.run(FastThreadLocalRunnable.java:30)
	at java.lang.Thread.run(Thread.java:750)
2023-06-15 04:55:58 INFO  [c.a.n.c.r.client              #printIfInfoEnabled  :  63] [6f26f36d-1d0a-4e1c-921a-5df4376c6d46] Fail to connect server, after trying 3 times, last try server is {serverIp = '127.0.0.1', server main port = 8848}, error = unknown
2023-06-15 04:55:58 ERROR [c.a.n.c.r.c.g.GrpcClient      #printIfErrorEnabled : 102] Server check fail, please check server 127.0.0.1 ,port 9848 is available , error ={}
java.util.concurrent.ExecutionException: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.getDoneValue(AbstractFuture.java:566)
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.get(AbstractFuture.java:445)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.serverCheck(GrpcClient.java:218)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.connectToServer(GrpcClient.java:329)
	at com.alibaba.nacos.common.remote.client.RpcClient.reconnect(RpcClient.java:502)
	at com.alibaba.nacos.common.remote.client.RpcClient.lambda$start$2(RpcClient.java:343)
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
	at java.util.concurrent.FutureTask.run(FutureTask.java:266)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.access$201(ScheduledThreadPoolExecutor.java:180)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:293)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)
Caused by: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.io.grpc.Status.asRuntimeException(Status.java:539)
	at com.alibaba.nacos.shaded.io.grpc.stub.ClientCalls$UnaryStreamToFuture.onClose(ClientCalls.java:544)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener$3.run(DelayedClientCall.java:471)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.delayOrExecute(DelayedClientCall.java:435)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.onClose(DelayedClientCall.java:468)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.closeObserver(ClientCallImpl.java:563)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.access$300(ClientCallImpl.java:70)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInternal(ClientCallImpl.java:744)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInContext(ClientCallImpl.java:723)
	at com.alibaba.nacos.shaded.io.grpc.internal.ContextRunnable.run(ContextRunnable.java:37)
	at com.alibaba.nacos.shaded.io.grpc.internal.SerializingExecutor.run(SerializingExecutor.java:133)
	... 3 common frames omitted
Caused by: com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.AbstractChannel$AnnotatedConnectException: Connection refused: /127.0.0.1:9848
Caused by: java.net.ConnectException: Connection refused
	at sun.nio.ch.SocketChannelImpl.checkConnect(Native Method)
	at sun.nio.ch.SocketChannelImpl.finishConnect(SocketChannelImpl.java:716)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.socket.nio.NioSocketChannel.doFinishConnect(NioSocketChannel.java:337)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.AbstractNioChannel$AbstractNioUnsafe.finishConnect(AbstractNioChannel.java:334)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKey(NioEventLoop.java:710)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeysOptimized(NioEventLoop.java:658)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeys(NioEventLoop.java:584)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.run(NioEventLoop.java:496)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.SingleThreadEventExecutor$4.run(SingleThreadEventExecutor.java:997)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.internal.ThreadExecutorMap$2.run(ThreadExecutorMap.java:74)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.FastThreadLocalRunnable.run(FastThreadLocalRunnable.java:30)
	at java.lang.Thread.run(Thread.java:750)
2023-06-15 04:55:58 INFO  [c.a.n.c.r.client              #printIfInfoEnabled  :  63] [05a9063c-6c77-43fd-8927-18776a5f500d] Fail to connect server, after trying 3 times, last try server is {serverIp = '127.0.0.1', server main port = 8848}, error = unknown
2023-06-15 04:55:58 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = ConfigPublishRequest{headers={charset=UTF-8, Client-AppName=unknown, Client-RequestToken=5b3c629ca65baf33f0c74d9ce8dfd8b2, Client-RequestTS=1686804958659, exConfigInfo=true}, requestId='null'}, retryTimes = 2, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:58 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = ConfigPublishRequest{headers={charset=UTF-8, Client-AppName=unknown, Client-RequestToken=5b3c629ca65baf33f0c74d9ce8dfd8b2, Client-RequestTS=1686804958659, exConfigInfo=true}, requestId='null'}, retryTimes = 2, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:58 WARN  [c.a.n.c.c.i.ClientWorker      #publishConfig       :1064] [fixed-127.0.0.1_8848] [publish-single] error, dataId=config.test.twOyaItMox, group=DEFAULT_GROUP, tenant=, code=unknown, msg=Client not connected, current status:STARTING
2023-06-15 04:55:58 WARN  [c.a.n.c.c.i.ClientWorker      #publishConfig       :1064] [fixed-127.0.0.1_8848] [publish-single] error, dataId=config.test.dfJwuzVwPZ, group=DEFAULT_GROUP, tenant=, code=unknown, msg=Client not connected, current status:STARTING
2023-06-15 04:55:58 INFO  [c.a.n.c.ConfigNormalTest      #ishAndAddOneListener:  93] publishConfig dataId:config.test.twOyaItMox, group:DEFAULT_GROUP, result:false



</details>

#### Name: [com.alibaba.nacos.config.ConfigNormalTest.testAddListenerAfterPublishConfig](https://github.com/nacos-group/nacos-e2e/tree/main/java/nacos-2X/src/test/java/com/alibaba/nacos/config/ConfigNormalTest.java#L292{:target="_blank"}) Time: 0.308s

<details>
<summary>Exception Detail</summary>


**Exception**
org.opentest4j.AssertionFailedError: expected: <true> but was: <false>
	at com.alibaba.nacos.config.ConfigNormalTest.testAddListenerAfterPublishConfig(ConfigNormalTest.java:292)

**System out info**
2023-06-15 04:55:51 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = ConfigPublishRequest{headers={charset=UTF-8, Client-AppName=unknown, Client-RequestToken=4532dca4fd9a7e1bac55115e8932540b, Client-RequestTS=1686804951511, exConfigInfo=true}, requestId='null'}, retryTimes = 2, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:51 WARN  [c.a.n.c.c.i.ClientWorker      #publishConfig       :1064] [fixed-127.0.0.1_8848] [publish-single] error, dataId=config.test.MoKFKXehHl, group=DEFAULT_GROUP, tenant=, code=unknown, msg=Client not connected, current status:STARTING
2023-06-15 04:55:51 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = ConfigPublishRequest{headers={charset=UTF-8, Client-AppName=unknown, Client-RequestToken=167488b70ed4b7b0d9ce8b04619f18a9, Client-RequestTS=1686804951631, exConfigInfo=true}, requestId='null'}, retryTimes = 1, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:51 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = SubscribeServiceRequest{headers={app=unknown}, requestId='null'}, retryTimes = 0, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:51 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = ConfigPublishRequest{headers={charset=UTF-8, Client-AppName=unknown, Client-RequestToken=7c369050fb73e2277776869e8da5b13c, Client-RequestTS=1686804951540, exConfigInfo=true}, requestId='null'}, retryTimes = 2, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:51 WARN  [c.a.n.c.c.i.ClientWorker      #publishConfig       :1064] [fixed-127.0.0.1_8848] [publish-single] error, dataId=config.test.FcHYmpXJNT, group=DEFAULT_GROUP, tenant=, code=unknown, msg=Client not connected, current status:STARTING
2023-06-15 04:55:51 INFO  [c.a.n.c.ConfigNormalTest      #erAfterPublishConfig: 291] publishConfig dataId:config.test.FcHYmpXJNT, group:DEFAULT_GROUP, result:false



</details>

#### Name: [com.alibaba.nacos.config.ConfigSyncTest.testClusterSync_addListenerAndRemoveListener2](https://github.com/nacos-group/nacos-e2e/tree/main/java/nacos-2X/src/test/java/com/alibaba/nacos/config/ConfigSyncTest.java#L196{:target="_blank"}) Time: 0.302s

<details>
<summary>Exception Detail</summary>


**Exception**
org.opentest4j.AssertionFailedError: expected: <true> but was: <false>
	at com.alibaba.nacos.config.ConfigSyncTest.testClusterSync_addListenerAndRemoveListener2(ConfigSyncTest.java:196)

**System out info**
2023-06-15 04:56:01 WARN  [c.a.n.c.naming                #run                 :  47] Grpc Connection is disconnect, skip current redo task
2023-06-15 04:56:01 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = ConfigQueryRequest{headers={charset=UTF-8, Client-AppName=unknown, Client-RequestToken=6ee606b2f3ba0ffb0910027906ec0ca2, Client-RequestTS=1686804960800, exConfigInfo=true, notify=false}, requestId='null'}, retryTimes = 2, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:56:01 WARN  [c.a.n.c.c.NacosConfigService  #getConfigInner      : 195] [fixed-127.0.0.1_8848] [get-config] get from server error, dataId=config.test.YWnPdRnqnY, group=DEFAULT_GROUP, tenant=, msg=ErrCode:-401, ErrMsg:Client not connected, current status:STARTING
2023-06-15 04:56:01 WARN  [c.a.n.c.naming                #run                 :  47] Grpc Connection is disconnect, skip current redo task
2023-06-15 04:56:01 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = ConfigPublishRequest{headers={charset=UTF-8, Client-AppName=unknown, Client-RequestToken=92d7b3f196bca01d8de92a4f3d6dd3d7, Client-RequestTS=1686804960815, exConfigInfo=true}, requestId='null'}, retryTimes = 2, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:56:01 WARN  [c.a.n.c.c.i.ClientWorker      #publishConfig       :1064] [fixed-127.0.0.1_8848] [publish-single] error, dataId=config.test.IvOzitlArH, group=DEFAULT_GROUP, tenant=, code=unknown, msg=Client not connected, current status:STARTING



</details>

#### Name: [com.alibaba.nacos.config.ConfigNormalTest.testAddTwoListener_removeLastListener](https://github.com/nacos-group/nacos-e2e/tree/main/java/nacos-2X/src/test/java/com/alibaba/nacos/config/ConfigNormalTest.java#L324{:target="_blank"}) Time: 0.304s

<details>
<summary>Exception Detail</summary>


**Exception**
org.opentest4j.AssertionFailedError: expected: <true> but was: <false>
	at com.alibaba.nacos.config.ConfigNormalTest.testAddTwoListener_removeLastListener(ConfigNormalTest.java:324)

**System out info**
2023-06-15 04:55:52 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = SubscribeServiceRequest{headers={app=unknown}, requestId='null'}, retryTimes = 0, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:52 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = ConfigPublishRequest{headers={charset=UTF-8, Client-AppName=unknown, Client-RequestToken=a6065aee4bd7e76bc5a48314c3c3e613, Client-RequestTS=1686804951849, exConfigInfo=true}, requestId='null'}, retryTimes = 2, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:52 WARN  [c.a.n.c.c.i.ClientWorker      #publishConfig       :1064] [fixed-127.0.0.1_8848] [publish-single] error, dataId=config.test.sacaJFdrNZ, group=DEFAULT_GROUP, tenant=, code=unknown, msg=Client not connected, current status:STARTING



</details>

#### Name: [com.alibaba.nacos.config.ConfigSyncTest.testClusterSync_addListenerAndRemoveListener](https://github.com/nacos-group/nacos-e2e/tree/main/java/nacos-2X/src/test/java/com/alibaba/nacos/config/ConfigSyncTest.java#L168{:target="_blank"}) Time: 0.303s

<details>
<summary>Exception Detail</summary>


**Exception**
org.opentest4j.AssertionFailedError: expected: <true> but was: <false>
	at com.alibaba.nacos.config.ConfigSyncTest.testClusterSync_addListenerAndRemoveListener(ConfigSyncTest.java:168)

**System out info**


</details>

#### Name: [com.alibaba.nacos.config.ConfigUnusualTest.testPublishAndGetConfig_specialCharacter](https://github.com/nacos-group/nacos-e2e/tree/main/java/nacos-2X/src/test/java/com/alibaba/nacos/config/ConfigUnusualTest.java#L174{:target="_blank"}) Time: 0.408s

<details>
<summary>Exception Detail</summary>


**Exception**
org.opentest4j.AssertionFailedError: publishConfig check fail ==> expected: <true> but was: <false>
	at com.alibaba.nacos.config.ConfigUnusualTest.testPublishAndGetConfig_specialCharacter(ConfigUnusualTest.java:174)

**System out info**
2023-06-15 04:55:58 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = ConfigPublishRequest{headers={charset=UTF-8, Client-AppName=unknown, Client-RequestToken=59572a797fba5058beea236ce99ddf58, Client-RequestTS=1686804958357, exConfigInfo=true}, requestId='null'}, retryTimes = 2, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:58 WARN  [c.a.n.c.c.i.ClientWorker      #publishConfig       :1064] [fixed-127.0.0.1_8848] [publish-single] error, dataId=config.test.xRZVrXQsNQ, group=DEFAULT_GROUP, tenant=, code=unknown, msg=Client not connected, current status:STARTING
2023-06-15 04:55:58 INFO  [c.a.n.c.ConfigUnusualTest     #fig_specialCharacter: 173] publishConfig dataId:config.test.xRZVrXQsNQ, group:DEFAULT_GROUP, result:false



</details>

#### Name: [com.alibaba.nacos.config.ConfigNormalTest.testPublishAndChangeConfig](https://github.com/nacos-group/nacos-e2e/tree/main/java/nacos-2X/src/test/java/com/alibaba/nacos/config/ConfigNormalTest.java#L198{:target="_blank"}) Time: 0.303s

<details>
<summary>Exception Detail</summary>


**Exception**
org.opentest4j.AssertionFailedError: expected: <true> but was: <false>
	at com.alibaba.nacos.config.ConfigNormalTest.testPublishAndChangeConfig(ConfigNormalTest.java:198)

**System out info**
2023-06-15 04:55:59 INFO  [c.a.n.n.SubscribeClusterTest  #setUp               :  39] Running test=Optional[public void com.alibaba.nacos.naming.SubscribeClusterTest.testSubscribeChangeWeight() throws java.lang.Exception], serviceName=nacos.MkaYk.jEvSU.com
2023-06-15 04:55:59 INFO  [c.a.n.c.naming                #registerService     : 121] [REGISTER-SERVICE] public registering service nacos.MkaYk.jEvSU.com with instance Instance{instanceId='null', ip='127.0.0.1', port=8848, weight=2.0, healthy=true, enabled=true, ephemeral=true, clusterName='c1', serviceName='nacos.MkaYk.jEvSU.com', metadata={site=et2}}
2023-06-15 04:55:59 INFO  [c.a.n.c.r.c.g.GrpcClient      #ateNewManagedChannel: 182] grpc client connection server:127.0.0.1 ip,serverPort:9848,grpcTslConfig:{"sslProvider":"","enableTls":false,"mutualAuthEnable":false,"trustAll":false}
2023-06-15 04:55:59 INFO  [c.a.n.c.r.c.g.GrpcClient      #ateNewManagedChannel: 182] grpc client connection server:127.0.0.1 ip,serverPort:9848,grpcTslConfig:{"sslProvider":"","enableTls":false,"mutualAuthEnable":false,"trustAll":false}
2023-06-15 04:55:59 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = SubscribeServiceRequest{headers={app=unknown}, requestId='null'}, retryTimes = 1, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:59 ERROR [c.a.n.c.r.c.g.GrpcClient      #printIfErrorEnabled : 102] Server check fail, please check server 127.0.0.1 ,port 9848 is available , error ={}
java.util.concurrent.ExecutionException: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.getDoneValue(AbstractFuture.java:566)
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.get(AbstractFuture.java:445)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.serverCheck(GrpcClient.java:218)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.connectToServer(GrpcClient.java:329)
	at com.alibaba.nacos.common.remote.client.RpcClient.reconnect(RpcClient.java:502)
	at com.alibaba.nacos.common.remote.client.RpcClient.lambda$start$2(RpcClient.java:343)
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
	at java.util.concurrent.FutureTask.run(FutureTask.java:266)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.access$201(ScheduledThreadPoolExecutor.java:180)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:293)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)
Caused by: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.io.grpc.Status.asRuntimeException(Status.java:539)
	at com.alibaba.nacos.shaded.io.grpc.stub.ClientCalls$UnaryStreamToFuture.onClose(ClientCalls.java:544)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener$3.run(DelayedClientCall.java:471)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.delayOrExecute(DelayedClientCall.java:435)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.onClose(DelayedClientCall.java:468)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.closeObserver(ClientCallImpl.java:563)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.access$300(ClientCallImpl.java:70)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInternal(ClientCallImpl.java:744)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInContext(ClientCallImpl.java:723)
	at com.alibaba.nacos.shaded.io.grpc.internal.ContextRunnable.run(ContextRunnable.java:37)
	at com.alibaba.nacos.shaded.io.grpc.internal.SerializingExecutor.run(SerializingExecutor.java:133)
	... 3 common frames omitted
Caused by: com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.AbstractChannel$AnnotatedConnectException: Connection refused: /127.0.0.1:9848
Caused by: java.net.ConnectException: Connection refused
	at sun.nio.ch.SocketChannelImpl.checkConnect(Native Method)
	at sun.nio.ch.SocketChannelImpl.finishConnect(SocketChannelImpl.java:716)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.socket.nio.NioSocketChannel.doFinishConnect(NioSocketChannel.java:337)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.AbstractNioChannel$AbstractNioUnsafe.finishConnect(AbstractNioChannel.java:334)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKey(NioEventLoop.java:710)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeysOptimized(NioEventLoop.java:658)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeys(NioEventLoop.java:584)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.run(NioEventLoop.java:496)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.SingleThreadEventExecutor$4.run(SingleThreadEventExecutor.java:997)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.internal.ThreadExecutorMap$2.run(ThreadExecutorMap.java:74)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.FastThreadLocalRunnable.run(FastThreadLocalRunnable.java:30)
	at java.lang.Thread.run(Thread.java:750)
2023-06-15 04:55:59 ERROR [c.a.n.c.r.c.g.GrpcClient      #printIfErrorEnabled : 102] Server check fail, please check server 127.0.0.1 ,port 9848 is available , error ={}
java.util.concurrent.ExecutionException: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.getDoneValue(AbstractFuture.java:566)
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.get(AbstractFuture.java:445)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.serverCheck(GrpcClient.java:218)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.connectToServer(GrpcClient.java:329)
	at com.alibaba.nacos.common.remote.client.RpcClient.reconnect(RpcClient.java:502)
	at com.alibaba.nacos.common.remote.client.RpcClient.lambda$start$2(RpcClient.java:343)
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
	at java.util.concurrent.FutureTask.run(FutureTask.java:266)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.access$201(ScheduledThreadPoolExecutor.java:180)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:293)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)
Caused by: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.io.grpc.Status.asRuntimeException(Status.java:539)
	at com.alibaba.nacos.shaded.io.grpc.stub.ClientCalls$UnaryStreamToFuture.onClose(ClientCalls.java:544)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener$3.run(DelayedClientCall.java:471)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.delayOrExecute(DelayedClientCall.java:435)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.onClose(DelayedClientCall.java:468)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.closeObserver(ClientCallImpl.java:563)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.access$300(ClientCallImpl.java:70)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInternal(ClientCallImpl.java:744)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInContext(ClientCallImpl.java:723)
	at com.alibaba.nacos.shaded.io.grpc.internal.ContextRunnable.run(ContextRunnable.java:37)
	at com.alibaba.nacos.shaded.io.grpc.internal.SerializingExecutor.run(SerializingExecutor.java:133)
	... 3 common frames omitted
Caused by: com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.AbstractChannel$AnnotatedConnectException: Connection refused: /127.0.0.1:9848
Caused by: java.net.ConnectException: Connection refused
	at sun.nio.ch.SocketChannelImpl.checkConnect(Native Method)
	at sun.nio.ch.SocketChannelImpl.finishConnect(SocketChannelImpl.java:716)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.socket.nio.NioSocketChannel.doFinishConnect(NioSocketChannel.java:337)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.AbstractNioChannel$AbstractNioUnsafe.finishConnect(AbstractNioChannel.java:334)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKey(NioEventLoop.java:710)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeysOptimized(NioEventLoop.java:658)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeys(NioEventLoop.java:584)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.run(NioEventLoop.java:496)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.SingleThreadEventExecutor$4.run(SingleThreadEventExecutor.java:997)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.internal.ThreadExecutorMap$2.run(ThreadExecutorMap.java:74)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.FastThreadLocalRunnable.run(FastThreadLocalRunnable.java:30)
	at java.lang.Thread.run(Thread.java:750)
2023-06-15 04:55:59 INFO  [c.a.n.c.r.client              #printIfInfoEnabled  :  63] [4714c6d0-2167-40dd-af8e-d61877c1be6c] Fail to connect server, after trying 13 times, last try server is {serverIp = '127.0.0.1', server main port = 8848}, error = unknown
2023-06-15 04:55:59 INFO  [c.a.n.c.r.client              #printIfInfoEnabled  :  63] [5a27e46d-dfd2-4a28-8e7f-f94825f4731f] Fail to connect server, after trying 13 times, last try server is {serverIp = '127.0.0.1', server main port = 8848}, error = unknown
2023-06-15 04:55:59 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = ConfigPublishRequest{headers={charset=UTF-8, Client-AppName=unknown, Client-RequestToken=5780e8e45642c56725cb8eee114adf6e, Client-RequestTS=1686804958962, exConfigInfo=true}, requestId='null'}, retryTimes = 2, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:59 WARN  [c.a.n.c.c.i.ClientWorker      #publishConfig       :1064] [fixed-127.0.0.1_8848] [publish-single] error, dataId=config.test.vdtIMjHcDp, group=DEFAULT_GROUP, tenant=, code=unknown, msg=Client not connected, current status:STARTING
2023-06-15 04:55:59 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = ConfigPublishRequest{headers={charset=UTF-8, Client-AppName=unknown, Client-RequestToken=5780e8e45642c56725cb8eee114adf6e, Client-RequestTS=1686804958962, exConfigInfo=true}, requestId='null'}, retryTimes = 2, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:59 INFO  [c.a.n.c.ConfigNormalTest      #blishAndChangeConfig: 197] publishConfig dataId:config.test.vdtIMjHcDp, group:DEFAULT_GROUP, result:false
2023-06-15 04:55:59 WARN  [c.a.n.c.c.i.ClientWorker      #publishConfig       :1064] [fixed-127.0.0.1_8848] [publish-single] error, dataId=config.test.fkGhXTZwCb, group=DEFAULT_GROUP, tenant=, code=unknown, msg=Client not connected, current status:STARTING



</details>

#### Name: [com.alibaba.nacos.config.ConfigSyncTest.testClusterSync_writeAndChange3](https://github.com/nacos-group/nacos-e2e/tree/main/java/nacos-2X/src/test/java/com/alibaba/nacos/config/ConfigSyncTest.java#L268{:target="_blank"}) Time: 0.387s

<details>
<summary>Exception Detail</summary>


**Exception**
org.opentest4j.AssertionFailedError: expected: <true> but was: <false>
	at com.alibaba.nacos.config.ConfigSyncTest.testClusterSync_writeAndChange3(ConfigSyncTest.java:268)

**System out info**
2023-06-15 04:55:58 INFO  [c.a.n.n.SubscribeClusterTest  #setUp               :  39] Running test=Optional[public void com.alibaba.nacos.naming.SubscribeClusterTest.testSubscribeOtherCluster() throws java.lang.Exception], serviceName=nacos.aZlFf.jerEj.net
2023-06-15 04:55:58 INFO  [c.a.n.c.naming                #subscribe           : 167] [SUBSCRIBE-SERVICE] service:nacos.aZlFf.jerEj.net, group:DEFAULT_GROUP, clusters:c2 
2023-06-15 04:55:58 DEBUG [c.a.n.c.naming                #subscribe           : 293] [GRPC-SUBSCRIBE] service:nacos.aZlFf.jerEj.net, group:DEFAULT_GROUP, cluster:c2 
2023-06-15 04:55:58 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = InstanceRequest{headers={app=unknown}, requestId='null'}, retryTimes = 1, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:58 INFO  [c.a.n.c.r.c.g.GrpcClient      #ateNewManagedChannel: 182] grpc client connection server:127.0.0.1 ip,serverPort:9848,grpcTslConfig:{"sslProvider":"","enableTls":false,"mutualAuthEnable":false,"trustAll":false}
2023-06-15 04:55:58 INFO  [c.a.n.c.r.c.g.GrpcClient      #ateNewManagedChannel: 182] grpc client connection server:127.0.0.1 ip,serverPort:9848,grpcTslConfig:{"sslProvider":"","enableTls":false,"mutualAuthEnable":false,"trustAll":false}
2023-06-15 04:55:58 ERROR [c.a.n.c.r.c.g.GrpcClient      #printIfErrorEnabled : 102] Server check fail, please check server 127.0.0.1 ,port 9848 is available , error ={}
java.util.concurrent.ExecutionException: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.getDoneValue(AbstractFuture.java:566)
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.get(AbstractFuture.java:445)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.serverCheck(GrpcClient.java:218)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.connectToServer(GrpcClient.java:329)
	at com.alibaba.nacos.common.remote.client.RpcClient.reconnect(RpcClient.java:502)
	at com.alibaba.nacos.common.remote.client.RpcClient.lambda$start$2(RpcClient.java:343)
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
	at java.util.concurrent.FutureTask.run(FutureTask.java:266)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.access$201(ScheduledThreadPoolExecutor.java:180)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:293)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)
Caused by: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.io.grpc.Status.asRuntimeException(Status.java:539)
	at com.alibaba.nacos.shaded.io.grpc.stub.ClientCalls$UnaryStreamToFuture.onClose(ClientCalls.java:544)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener$3.run(DelayedClientCall.java:471)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.delayOrExecute(DelayedClientCall.java:435)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.onClose(DelayedClientCall.java:468)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.closeObserver(ClientCallImpl.java:563)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.access$300(ClientCallImpl.java:70)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInternal(ClientCallImpl.java:744)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInContext(ClientCallImpl.java:723)
	at com.alibaba.nacos.shaded.io.grpc.internal.ContextRunnable.run(ContextRunnable.java:37)
	at com.alibaba.nacos.shaded.io.grpc.internal.SerializingExecutor.run(SerializingExecutor.java:133)
	... 3 common frames omitted
Caused by: com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.AbstractChannel$AnnotatedConnectException: Connection refused: /127.0.0.1:9848
Caused by: java.net.ConnectException: Connection refused
	at sun.nio.ch.SocketChannelImpl.checkConnect(Native Method)
	at sun.nio.ch.SocketChannelImpl.finishConnect(SocketChannelImpl.java:716)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.socket.nio.NioSocketChannel.doFinishConnect(NioSocketChannel.java:337)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.AbstractNioChannel$AbstractNioUnsafe.finishConnect(AbstractNioChannel.java:334)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKey(NioEventLoop.java:710)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeysOptimized(NioEventLoop.java:658)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeys(NioEventLoop.java:584)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.run(NioEventLoop.java:496)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.SingleThreadEventExecutor$4.run(SingleThreadEventExecutor.java:997)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.internal.ThreadExecutorMap$2.run(ThreadExecutorMap.java:74)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.FastThreadLocalRunnable.run(FastThreadLocalRunnable.java:30)
	at java.lang.Thread.run(Thread.java:750)
2023-06-15 04:55:58 INFO  [c.a.n.c.r.client              #printIfInfoEnabled  :  63] [6f26f36d-1d0a-4e1c-921a-5df4376c6d46] Fail to connect server, after trying 2 times, last try server is {serverIp = '127.0.0.1', server main port = 8848}, error = unknown
2023-06-15 04:55:58 ERROR [c.a.n.c.r.c.g.GrpcClient      #printIfErrorEnabled : 102] Server check fail, please check server 127.0.0.1 ,port 9848 is available , error ={}
java.util.concurrent.ExecutionException: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.getDoneValue(AbstractFuture.java:566)
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.get(AbstractFuture.java:445)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.serverCheck(GrpcClient.java:218)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.connectToServer(GrpcClient.java:329)
	at com.alibaba.nacos.common.remote.client.RpcClient.reconnect(RpcClient.java:502)
	at com.alibaba.nacos.common.remote.client.RpcClient.lambda$start$2(RpcClient.java:343)
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
	at java.util.concurrent.FutureTask.run(FutureTask.java:266)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.access$201(ScheduledThreadPoolExecutor.java:180)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:293)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)
Caused by: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.io.grpc.Status.asRuntimeException(Status.java:539)
	at com.alibaba.nacos.shaded.io.grpc.stub.ClientCalls$UnaryStreamToFuture.onClose(ClientCalls.java:544)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener$3.run(DelayedClientCall.java:471)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.delayOrExecute(DelayedClientCall.java:435)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.onClose(DelayedClientCall.java:468)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.closeObserver(ClientCallImpl.java:563)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.access$300(ClientCallImpl.java:70)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInternal(ClientCallImpl.java:744)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInContext(ClientCallImpl.java:723)
	at com.alibaba.nacos.shaded.io.grpc.internal.ContextRunnable.run(ContextRunnable.java:37)
	at com.alibaba.nacos.shaded.io.grpc.internal.SerializingExecutor.run(SerializingExecutor.java:133)
	... 3 common frames omitted
Caused by: com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.AbstractChannel$AnnotatedConnectException: Connection refused: /127.0.0.1:9848
Caused by: java.net.ConnectException: Connection refused
	at sun.nio.ch.SocketChannelImpl.checkConnect(Native Method)
	at sun.nio.ch.SocketChannelImpl.finishConnect(SocketChannelImpl.java:716)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.socket.nio.NioSocketChannel.doFinishConnect(NioSocketChannel.java:337)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.AbstractNioChannel$AbstractNioUnsafe.finishConnect(AbstractNioChannel.java:334)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKey(NioEventLoop.java:710)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeysOptimized(NioEventLoop.java:658)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeys(NioEventLoop.java:584)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.run(NioEventLoop.java:496)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.SingleThreadEventExecutor$4.run(SingleThreadEventExecutor.java:997)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.internal.ThreadExecutorMap$2.run(ThreadExecutorMap.java:74)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.FastThreadLocalRunnable.run(FastThreadLocalRunnable.java:30)
	at java.lang.Thread.run(Thread.java:750)
2023-06-15 04:55:58 INFO  [c.a.n.c.r.client              #printIfInfoEnabled  :  63] [05a9063c-6c77-43fd-8927-18776a5f500d] Fail to connect server, after trying 2 times, last try server is {serverIp = '127.0.0.1', server main port = 8848}, error = unknown
2023-06-15 04:55:58 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = ConfigPublishRequest{headers={charset=UTF-8, Client-AppName=unknown, Client-RequestToken=80b3ff8b655188e72d5528f7d857ffda, Client-RequestTS=1686804958356, exConfigInfo=true}, requestId='null'}, retryTimes = 2, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:58 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = ConfigPublishRequest{headers={charset=UTF-8, Client-AppName=unknown, Client-RequestToken=80b3ff8b655188e72d5528f7d857ffda, Client-RequestTS=1686804958356, exConfigInfo=true}, requestId='null'}, retryTimes = 2, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:55:58 WARN  [c.a.n.c.c.i.ClientWorker      #publishConfig       :1064] [fixed-127.0.0.1_8848] [publish-single] error, dataId=config.test.jAlwljlJds, group=DEFAULT_GROUP, tenant=, code=unknown, msg=Client not connected, current status:STARTING
2023-06-15 04:55:58 WARN  [c.a.n.c.c.i.ClientWorker      #publishConfig       :1064] [fixed-127.0.0.1_8848] [publish-single] error, dataId=config.test.aRLpwpcdCD, group=DEFAULT_GROUP, tenant=, code=unknown, msg=Client not connected, current status:STARTING
2023-06-15 04:55:58 INFO  [c.a.n.c.ConfigNormalTest      #testRemoveConfig    : 178] publishConfig dataId:config.test.jAlwljlJds, group:DEFAULT_GROUP, result:false



</details>

#### Name: [com.alibaba.nacos.config.ConfigSyncTest.testClusterSync_writeAndChange2](https://github.com/nacos-group/nacos-e2e/tree/main/java/nacos-2X/src/test/java/com/alibaba/nacos/config/ConfigSyncTest.java#L239{:target="_blank"}) Time: 0.303s

<details>
<summary>Exception Detail</summary>


**Exception**
org.opentest4j.AssertionFailedError: expected: <true> but was: <false>
	at com.alibaba.nacos.config.ConfigSyncTest.testClusterSync_writeAndChange2(ConfigSyncTest.java:239)

**System out info**
2023-06-15 04:56:01 INFO  [c.a.n.c.r.client              #printIfInfoEnabled  :  63] [05a9063c-6c77-43fd-8927-18776a5f500d] Fail to connect server, after trying 7 times, last try server is {serverIp = '127.0.0.1', server main port = 8848}, error = unknown
2023-06-15 04:56:01 INFO  [c.a.n.n.MultiTenantTest       #setUp               :  66] Running test=Optional[public void com.alibaba.nacos.naming.MultiTenantTest.testMultipleTenant_registerInstance() throws java.lang.Exception], serviceName=nacos.yQiBf.vIYUK.net
2023-06-15 04:56:01 INFO  [c.a.n.c.naming                #registerService     : 121] [REGISTER-SERVICE] public registering service nacos.yQiBf.vIYUK.net with instance Instance{instanceId='null', ip='33.33.33.33', port=8888, weight=1.0, healthy=true, enabled=true, ephemeral=true, clusterName='DEFAULT', serviceName='null', metadata={}}
2023-06-15 04:56:01 INFO  [c.a.n.c.r.c.g.GrpcClient      #ateNewManagedChannel: 182] grpc client connection server:127.0.0.1 ip,serverPort:9848,grpcTslConfig:{"sslProvider":"","enableTls":false,"mutualAuthEnable":false,"trustAll":false}
2023-06-15 04:56:01 ERROR [c.a.n.c.r.c.g.GrpcClient      #printIfErrorEnabled : 102] Server check fail, please check server 127.0.0.1 ,port 9848 is available , error ={}
java.util.concurrent.ExecutionException: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.getDoneValue(AbstractFuture.java:566)
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.get(AbstractFuture.java:445)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.serverCheck(GrpcClient.java:218)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.connectToServer(GrpcClient.java:329)
	at com.alibaba.nacos.common.remote.client.RpcClient.reconnect(RpcClient.java:502)
	at com.alibaba.nacos.common.remote.client.RpcClient.lambda$start$2(RpcClient.java:343)
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
	at java.util.concurrent.FutureTask.run(FutureTask.java:266)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.access$201(ScheduledThreadPoolExecutor.java:180)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:293)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)
Caused by: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.io.grpc.Status.asRuntimeException(Status.java:539)
	at com.alibaba.nacos.shaded.io.grpc.stub.ClientCalls$UnaryStreamToFuture.onClose(ClientCalls.java:544)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener$3.run(DelayedClientCall.java:471)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.delayOrExecute(DelayedClientCall.java:435)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.onClose(DelayedClientCall.java:468)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.closeObserver(ClientCallImpl.java:563)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.access$300(ClientCallImpl.java:70)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInternal(ClientCallImpl.java:744)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInContext(ClientCallImpl.java:723)
	at com.alibaba.nacos.shaded.io.grpc.internal.ContextRunnable.run(ContextRunnable.java:37)
	at com.alibaba.nacos.shaded.io.grpc.internal.SerializingExecutor.run(SerializingExecutor.java:133)
	... 3 common frames omitted
Caused by: com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.AbstractChannel$AnnotatedConnectException: Connection refused: /127.0.0.1:9848
Caused by: java.net.ConnectException: Connection refused
	at sun.nio.ch.SocketChannelImpl.checkConnect(Native Method)
	at sun.nio.ch.SocketChannelImpl.finishConnect(SocketChannelImpl.java:716)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.socket.nio.NioSocketChannel.doFinishConnect(NioSocketChannel.java:337)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.AbstractNioChannel$AbstractNioUnsafe.finishConnect(AbstractNioChannel.java:334)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKey(NioEventLoop.java:710)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeysOptimized(NioEventLoop.java:658)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeys(NioEventLoop.java:584)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.run(NioEventLoop.java:496)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.SingleThreadEventExecutor$4.run(SingleThreadEventExecutor.java:997)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.internal.ThreadExecutorMap$2.run(ThreadExecutorMap.java:74)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.FastThreadLocalRunnable.run(FastThreadLocalRunnable.java:30)
	at java.lang.Thread.run(Thread.java:750)
2023-06-15 04:56:01 INFO  [c.a.n.c.r.client              #printIfInfoEnabled  :  63] [60abd0fe-26b4-4d74-96b1-2f66d466f669] Fail to connect server, after trying 7 times, last try server is {serverIp = '127.0.0.1', server main port = 8848}, error = unknown
2023-06-15 04:56:01 INFO  [c.a.n.c.r.c.g.GrpcClient      #ateNewManagedChannel: 182] grpc client connection server:127.0.0.1 ip,serverPort:9848,grpcTslConfig:{"sslProvider":"","enableTls":false,"mutualAuthEnable":false,"trustAll":false}
2023-06-15 04:56:01 ERROR [c.a.n.c.r.c.g.GrpcClient      #printIfErrorEnabled : 102] Server check fail, please check server 127.0.0.1 ,port 9848 is available , error ={}
java.util.concurrent.ExecutionException: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.getDoneValue(AbstractFuture.java:566)
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.get(AbstractFuture.java:445)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.serverCheck(GrpcClient.java:218)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.connectToServer(GrpcClient.java:329)
	at com.alibaba.nacos.common.remote.client.RpcClient.reconnect(RpcClient.java:502)
	at com.alibaba.nacos.common.remote.client.RpcClient.lambda$start$2(RpcClient.java:343)
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
	at java.util.concurrent.FutureTask.run(FutureTask.java:266)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.access$201(ScheduledThreadPoolExecutor.java:180)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:293)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)
Caused by: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.io.grpc.Status.asRuntimeException(Status.java:539)
	at com.alibaba.nacos.shaded.io.grpc.stub.ClientCalls$UnaryStreamToFuture.onClose(ClientCalls.java:544)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener$3.run(DelayedClientCall.java:471)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.delayOrExecute(DelayedClientCall.java:435)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.onClose(DelayedClientCall.java:468)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.closeObserver(ClientCallImpl.java:563)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.access$300(ClientCallImpl.java:70)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInternal(ClientCallImpl.java:744)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInContext(ClientCallImpl.java:723)
	at com.alibaba.nacos.shaded.io.grpc.internal.ContextRunnable.run(ContextRunnable.java:37)
	at com.alibaba.nacos.shaded.io.grpc.internal.SerializingExecutor.run(SerializingExecutor.java:133)
	... 3 common frames omitted
Caused by: com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.AbstractChannel$AnnotatedConnectException: Connection refused: /127.0.0.1:9848
Caused by: java.net.ConnectException: Connection refused
	at sun.nio.ch.SocketChannelImpl.checkConnect(Native Method)
	at sun.nio.ch.SocketChannelImpl.finishConnect(SocketChannelImpl.java:716)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.socket.nio.NioSocketChannel.doFinishConnect(NioSocketChannel.java:337)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.AbstractNioChannel$AbstractNioUnsafe.finishConnect(AbstractNioChannel.java:334)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKey(NioEventLoop.java:710)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeysOptimized(NioEventLoop.java:658)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeys(NioEventLoop.java:584)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.run(NioEventLoop.java:496)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.SingleThreadEventExecutor$4.run(SingleThreadEventExecutor.java:997)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.internal.ThreadExecutorMap$2.run(ThreadExecutorMap.java:74)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.FastThreadLocalRunnable.run(FastThreadLocalRunnable.java:30)
	at java.lang.Thread.run(Thread.java:750)
2023-06-15 04:56:01 INFO  [c.a.n.c.r.client              #printIfInfoEnabled  :  63] [17ba6433-d199-490b-98b0-01210bb6c13e] Fail to connect server, after trying 4 times, last try server is {serverIp = '127.0.0.1', server main port = 8848}, error = unknown
2023-06-15 04:56:01 INFO  [c.a.n.c.r.c.g.GrpcClient      #ateNewManagedChannel: 182] grpc client connection server:127.0.0.1 ip,serverPort:9848,grpcTslConfig:{"sslProvider":"","enableTls":false,"mutualAuthEnable":false,"trustAll":false}
2023-06-15 04:56:01 ERROR [c.a.n.c.r.c.g.GrpcClient      #printIfErrorEnabled : 102] Server check fail, please check server 127.0.0.1 ,port 9848 is available , error ={}
java.util.concurrent.ExecutionException: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.getDoneValue(AbstractFuture.java:566)
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.get(AbstractFuture.java:445)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.serverCheck(GrpcClient.java:218)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.connectToServer(GrpcClient.java:329)
	at com.alibaba.nacos.common.remote.client.RpcClient.reconnect(RpcClient.java:502)
	at com.alibaba.nacos.common.remote.client.RpcClient.lambda$start$2(RpcClient.java:343)
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
	at java.util.concurrent.FutureTask.run(FutureTask.java:266)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.access$201(ScheduledThreadPoolExecutor.java:180)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:293)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)
Caused by: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.io.grpc.Status.asRuntimeException(Status.java:539)
	at com.alibaba.nacos.shaded.io.grpc.stub.ClientCalls$UnaryStreamToFuture.onClose(ClientCalls.java:544)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener$3.run(DelayedClientCall.java:471)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.delayOrExecute(DelayedClientCall.java:435)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.onClose(DelayedClientCall.java:468)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.closeObserver(ClientCallImpl.java:563)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.access$300(ClientCallImpl.java:70)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInternal(ClientCallImpl.java:744)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInContext(ClientCallImpl.java:723)
	at com.alibaba.nacos.shaded.io.grpc.internal.ContextRunnable.run(ContextRunnable.java:37)
	at com.alibaba.nacos.shaded.io.grpc.internal.SerializingExecutor.run(SerializingExecutor.java:133)
	... 3 common frames omitted
Caused by: com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.AbstractChannel$AnnotatedConnectException: Connection refused: /127.0.0.1:9848
Caused by: java.net.ConnectException: Connection refused
	at sun.nio.ch.SocketChannelImpl.checkConnect(Native Method)
	at sun.nio.ch.SocketChannelImpl.finishConnect(SocketChannelImpl.java:716)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.socket.nio.NioSocketChannel.doFinishConnect(NioSocketChannel.java:337)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.AbstractNioChannel$AbstractNioUnsafe.finishConnect(AbstractNioChannel.java:334)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKey(NioEventLoop.java:710)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeysOptimized(NioEventLoop.java:658)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeys(NioEventLoop.java:584)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.run(NioEventLoop.java:496)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.SingleThreadEventExecutor$4.run(SingleThreadEventExecutor.java:997)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.internal.ThreadExecutorMap$2.run(ThreadExecutorMap.java:74)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.FastThreadLocalRunnable.run(FastThreadLocalRunnable.java:30)
	at java.lang.Thread.run(Thread.java:750)
2023-06-15 04:56:01 INFO  [c.a.n.c.r.client              #printIfInfoEnabled  :  63] [16e8cae7-9ee0-453c-88cb-18279dc17637] Fail to connect server, after trying 8 times, last try server is {serverIp = '127.0.0.1', server main port = 8848}, error = unknown
2023-06-15 04:56:01 INFO  [c.a.n.c.r.c.g.GrpcClient      #ateNewManagedChannel: 182] grpc client connection server:127.0.0.1 ip,serverPort:9848,grpcTslConfig:{"sslProvider":"","enableTls":false,"mutualAuthEnable":false,"trustAll":false}
2023-06-15 04:56:01 ERROR [c.a.n.c.r.c.g.GrpcClient      #printIfErrorEnabled : 102] Server check fail, please check server 127.0.0.1 ,port 9848 is available , error ={}
java.util.concurrent.ExecutionException: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.getDoneValue(AbstractFuture.java:566)
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.get(AbstractFuture.java:445)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.serverCheck(GrpcClient.java:218)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.connectToServer(GrpcClient.java:329)
	at com.alibaba.nacos.common.remote.client.RpcClient.reconnect(RpcClient.java:502)
	at com.alibaba.nacos.common.remote.client.RpcClient.lambda$start$2(RpcClient.java:343)
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
	at java.util.concurrent.FutureTask.run(FutureTask.java:266)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.access$201(ScheduledThreadPoolExecutor.java:180)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:293)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)
Caused by: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.io.grpc.Status.asRuntimeException(Status.java:539)
	at com.alibaba.nacos.shaded.io.grpc.stub.ClientCalls$UnaryStreamToFuture.onClose(ClientCalls.java:544)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener$3.run(DelayedClientCall.java:471)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.delayOrExecute(DelayedClientCall.java:435)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.onClose(DelayedClientCall.java:468)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.closeObserver(ClientCallImpl.java:563)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.access$300(ClientCallImpl.java:70)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInternal(ClientCallImpl.java:744)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInContext(ClientCallImpl.java:723)
	at com.alibaba.nacos.shaded.io.grpc.internal.ContextRunnable.run(ContextRunnable.java:37)
	at com.alibaba.nacos.shaded.io.grpc.internal.SerializingExecutor.run(SerializingExecutor.java:133)
	... 3 common frames omitted
Caused by: com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.AbstractChannel$AnnotatedConnectException: Connection refused: /127.0.0.1:9848
Caused by: java.net.ConnectException: Connection refused
	at sun.nio.ch.SocketChannelImpl.checkConnect(Native Method)
	at sun.nio.ch.SocketChannelImpl.finishConnect(SocketChannelImpl.java:716)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.socket.nio.NioSocketChannel.doFinishConnect(NioSocketChannel.java:337)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.AbstractNioChannel$AbstractNioUnsafe.finishConnect(AbstractNioChannel.java:334)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKey(NioEventLoop.java:710)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeysOptimized(NioEventLoop.java:658)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeys(NioEventLoop.java:584)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.run(NioEventLoop.java:496)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.SingleThreadEventExecutor$4.run(SingleThreadEventExecutor.java:997)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.internal.ThreadExecutorMap$2.run(ThreadExecutorMap.java:74)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.FastThreadLocalRunnable.run(FastThreadLocalRunnable.java:30)
	at java.lang.Thread.run(Thread.java:750)
2023-06-15 04:56:01 INFO  [c.a.n.c.r.client              #printIfInfoEnabled  :  63] [67c8841a-cc93-490c-9daf-49ef0a650b16_config-0] Fail to connect server, after trying 7 times, last try server is {serverIp = '127.0.0.1', server main port = 8848}, error = unknown
2023-06-15 04:56:01 INFO  [c.a.n.c.r.c.g.GrpcClient      #ateNewManagedChannel: 182] grpc client connection server:127.0.0.1 ip,serverPort:9848,grpcTslConfig:{"sslProvider":"","enableTls":false,"mutualAuthEnable":false,"trustAll":false}
2023-06-15 04:56:01 ERROR [c.a.n.c.r.c.g.GrpcClient      #printIfErrorEnabled : 102] Server check fail, please check server 127.0.0.1 ,port 9848 is available , error ={}
java.util.concurrent.ExecutionException: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.getDoneValue(AbstractFuture.java:566)
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.get(AbstractFuture.java:445)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.serverCheck(GrpcClient.java:218)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.connectToServer(GrpcClient.java:329)
	at com.alibaba.nacos.common.remote.client.RpcClient.reconnect(RpcClient.java:502)
	at com.alibaba.nacos.common.remote.client.RpcClient.lambda$start$2(RpcClient.java:343)
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
	at java.util.concurrent.FutureTask.run(FutureTask.java:266)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.access$201(ScheduledThreadPoolExecutor.java:180)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:293)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)
Caused by: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.io.grpc.Status.asRuntimeException(Status.java:539)
	at com.alibaba.nacos.shaded.io.grpc.stub.ClientCalls$UnaryStreamToFuture.onClose(ClientCalls.java:544)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener$3.run(DelayedClientCall.java:471)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.delayOrExecute(DelayedClientCall.java:435)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.onClose(DelayedClientCall.java:468)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.closeObserver(ClientCallImpl.java:563)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.access$300(ClientCallImpl.java:70)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInternal(ClientCallImpl.java:744)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInContext(ClientCallImpl.java:723)
	at com.alibaba.nacos.shaded.io.grpc.internal.ContextRunnable.run(ContextRunnable.java:37)
	at com.alibaba.nacos.shaded.io.grpc.internal.SerializingExecutor.run(SerializingExecutor.java:133)
	... 3 common frames omitted
Caused by: com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.AbstractChannel$AnnotatedConnectException: Connection refused: /127.0.0.1:9848
Caused by: java.net.ConnectException: Connection refused
	at sun.nio.ch.SocketChannelImpl.checkConnect(Native Method)
	at sun.nio.ch.SocketChannelImpl.finishConnect(SocketChannelImpl.java:716)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.socket.nio.NioSocketChannel.doFinishConnect(NioSocketChannel.java:337)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.AbstractNioChannel$AbstractNioUnsafe.finishConnect(AbstractNioChannel.java:334)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKey(NioEventLoop.java:710)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeysOptimized(NioEventLoop.java:658)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeys(NioEventLoop.java:584)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.run(NioEventLoop.java:496)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.SingleThreadEventExecutor$4.run(SingleThreadEventExecutor.java:997)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.internal.ThreadExecutorMap$2.run(ThreadExecutorMap.java:74)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.FastThreadLocalRunnable.run(FastThreadLocalRunnable.java:30)
	at java.lang.Thread.run(Thread.java:750)
2023-06-15 04:56:01 INFO  [c.a.n.c.r.client              #printIfInfoEnabled  :  63] [861c454e-1557-4606-83c2-b4c0ee7cb551] Fail to connect server, after trying 4 times, last try server is {serverIp = '127.0.0.1', server main port = 8848}, error = unknown
2023-06-15 04:56:01 INFO  [c.a.n.c.r.c.g.GrpcClient      #ateNewManagedChannel: 182] grpc client connection server:127.0.0.1 ip,serverPort:9848,grpcTslConfig:{"sslProvider":"","enableTls":false,"mutualAuthEnable":false,"trustAll":false}
2023-06-15 04:56:01 ERROR [c.a.n.c.r.c.g.GrpcClient      #printIfErrorEnabled : 102] Server check fail, please check server 127.0.0.1 ,port 9848 is available , error ={}
java.util.concurrent.ExecutionException: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.getDoneValue(AbstractFuture.java:566)
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.get(AbstractFuture.java:445)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.serverCheck(GrpcClient.java:218)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.connectToServer(GrpcClient.java:329)
	at com.alibaba.nacos.common.remote.client.RpcClient.reconnect(RpcClient.java:502)
	at com.alibaba.nacos.common.remote.client.RpcClient.lambda$start$2(RpcClient.java:343)
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
	at java.util.concurrent.FutureTask.run(FutureTask.java:266)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.access$201(ScheduledThreadPoolExecutor.java:180)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:293)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)
Caused by: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.io.grpc.Status.asRuntimeException(Status.java:539)
	at com.alibaba.nacos.shaded.io.grpc.stub.ClientCalls$UnaryStreamToFuture.onClose(ClientCalls.java:544)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener$3.run(DelayedClientCall.java:471)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.delayOrExecute(DelayedClientCall.java:435)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.onClose(DelayedClientCall.java:468)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.closeObserver(ClientCallImpl.java:563)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl.access$300(ClientCallImpl.java:70)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInternal(ClientCallImpl.java:744)
	at com.alibaba.nacos.shaded.io.grpc.internal.ClientCallImpl$ClientStreamListenerImpl$1StreamClosed.runInContext(ClientCallImpl.java:723)
	at com.alibaba.nacos.shaded.io.grpc.internal.ContextRunnable.run(ContextRunnable.java:37)
	at com.alibaba.nacos.shaded.io.grpc.internal.SerializingExecutor.run(SerializingExecutor.java:133)
	... 3 common frames omitted
Caused by: com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.AbstractChannel$AnnotatedConnectException: Connection refused: /127.0.0.1:9848
Caused by: java.net.ConnectException: Connection refused
	at sun.nio.ch.SocketChannelImpl.checkConnect(Native Method)
	at sun.nio.ch.SocketChannelImpl.finishConnect(SocketChannelImpl.java:716)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.socket.nio.NioSocketChannel.doFinishConnect(NioSocketChannel.java:337)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.AbstractNioChannel$AbstractNioUnsafe.finishConnect(AbstractNioChannel.java:334)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKey(NioEventLoop.java:710)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeysOptimized(NioEventLoop.java:658)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.processSelectedKeys(NioEventLoop.java:584)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.channel.nio.NioEventLoop.run(NioEventLoop.java:496)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.SingleThreadEventExecutor$4.run(SingleThreadEventExecutor.java:997)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.internal.ThreadExecutorMap$2.run(ThreadExecutorMap.java:74)
	at com.alibaba.nacos.shaded.io.grpc.netty.shaded.io.netty.util.concurrent.FastThreadLocalRunnable.run(FastThreadLocalRunnable.java:30)
	at java.lang.Thread.run(Thread.java:750)
2023-06-15 04:56:01 INFO  [c.a.n.c.r.client              #printIfInfoEnabled  :  63] [5fc54880-7ba4-488c-9f12-3f4e2cb128f3_config-0] Fail to connect server, after trying 7 times, last try server is {serverIp = '127.0.0.1', server main port = 8848}, error = unknown
2023-06-15 04:56:01 ERROR [c.a.n.c.r.client              #printIfErrorEnabled : 102] Send request fail, request = ConfigPublishRequest{headers={charset=UTF-8, Client-AppName=unknown, Client-RequestToken=778ad2a1266c960e7744c12a38ef812a, Client-RequestTS=1686804961094, exConfigInfo=true}, requestId='null'}, retryTimes = 0, errorMessage = Client not connected, current status:STARTING
2023-06-15 04:56:01 INFO  [c.a.n.c.r.c.g.GrpcClient      #ateNewManagedChannel: 182] grpc client connection server:127.0.0.1 ip,serverPort:9848,grpcTslConfig:{"sslProvider":"","enableTls":false,"mutualAuthEnable":false,"trustAll":false}
2023-06-15 04:56:01 ERROR [c.a.n.c.r.c.g.GrpcClient      #printIfErrorEnabled : 102] Server check fail, please check server 127.0.0.1 ,port 9848 is available , error ={}
java.util.concurrent.ExecutionException: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.getDoneValue(AbstractFuture.java:566)
	at com.alibaba.nacos.shaded.com.google.common.util.concurrent.AbstractFuture.get(AbstractFuture.java:445)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.serverCheck(GrpcClient.java:218)
	at com.alibaba.nacos.common.remote.client.grpc.GrpcClient.connectToServer(GrpcClient.java:329)
	at com.alibaba.nacos.common.remote.client.RpcClient.reconnect(RpcClient.java:502)
	at com.alibaba.nacos.common.remote.client.RpcClient.lambda$start$2(RpcClient.java:343)
	at java.util.concurrent.Executors$RunnableAdapter.call(Executors.java:511)
	at java.util.concurrent.FutureTask.run(FutureTask.java:266)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.access$201(ScheduledThreadPoolExecutor.java:180)
	at java.util.concurrent.ScheduledThreadPoolExecutor$ScheduledFutureTask.run(ScheduledThreadPoolExecutor.java:293)
	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1149)
	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:624)
	at java.lang.Thread.run(Thread.java:750)
Caused by: com.alibaba.nacos.shaded.io.grpc.StatusRuntimeException: UNAVAILABLE: io exception
	at com.alibaba.nacos.shaded.io.grpc.Status.asRuntimeException(Status.java:539)
	at com.alibaba.nacos.shaded.io.grpc.stub.ClientCalls$UnaryStreamToFuture.onClose(ClientCalls.java:544)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener$3.run(DelayedClientCall.java:471)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.delayOrExecute(DelayedClientCall.java:435)
	at com.alibaba.nacos.shaded.io.grpc.internal.DelayedClientCall$DelayedListener.onClose(DelayedClientCall.java:468)
	at com.alibaba.nacos.shaded.i
