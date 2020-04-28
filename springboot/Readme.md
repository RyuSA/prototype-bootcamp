# Springboot

## 手順
### 初期起動まで(時間かかるので、ここまでは先にやっておいてもらう)

1. cloneしてくる
```
git clone me
```

2. あげる
```
docker-compose up
```

3. コンテナにアタッチ（おすすめはVSCodeのRemoteDevelopmentでのAttach）
```
docker exec ...
```

4. (VSCodeのRemoteDevelopmentの人のみ) 拡張機能「JavaExtention」のインストール(任意)


5. /appに移動（Dockerfileに書いてある通り、/appが作業Dir）
6. bootRunする(説明は後述)(必要なモジュールとか諸々持ってくるので、マシンスペックによっては10分近くかかる)
```
./gradlew bootRun
```

7. 下記のSpringboot初期起動まで確認出来ることを確認
```
  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::        (v2.2.4.RELEASE)

2020-04-27 13:29:18.358  INFO 4124 --- [  restartedMain] com.example.demo.DemoApplication         : Starting DemoApplication on 2b1ec461b14e with PID 4124 (/app/build/classes/java/main started by root in /app)
2020-04-27 13:29:18.364  INFO 4124 --- [  restartedMain] com.example.demo.DemoApplication         : No active profile set, falling back to default profiles: default
2020-04-27 13:29:18.494  INFO 4124 --- [  restartedMain] .e.DevToolsPropertyDefaultsPostProcessor : Devtools property defaults active! Set 'spring.devtools.add-properties' to 'false' to disabl
2020-04-27 13:29:18.495  INFO 4124 --- [  restartedMain] .e.DevToolsPropertyDefaultsPostProcessor : For additional web related logging consider setting the 'logging.level.web' property to 'DEBUG'
2020-04-27 13:29:19.591  INFO 4124 --- [  restartedMain] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat initialized with port(s): 8080 (http)
2020-04-27 13:29:19.604  INFO 4124 --- [  restartedMain] o.apache.catalina.core.StandardService   : Starting service [Tomcat]
2020-04-27 13:29:19.605  INFO 4124 --- [  restartedMain] org.apache.catalina.core.StandardEngine  : Starting Servlet engine: [Apache Tomcat/9.0.30]
2020-04-27 13:29:19.701  INFO 4124 --- [  restartedMain] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring embedded WebApplicationContext
2020-04-27 13:29:19.701  INFO 4124 --- [  restartedMain] o.s.web.context.ContextLoader            : Root WebApplicationContext: initialization completed in 1206 ms
2020-04-27 13:29:19.971  INFO 4124 --- [  restartedMain] o.s.s.concurrent.ThreadPoolTaskExecutor  : Initializing ExecutorService 'applicationTaskExecutor'
2020-04-27 13:29:20.165  INFO 4124 --- [  restartedMain] o.s.b.d.a.OptionalLiveReloadServer       : LiveReload server is running on port 35729
2020-04-27 13:29:20.211  INFO 4124 --- [  restartedMain] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat started on port(s): 8080 (http) with context path ''
2020-04-27 13:29:20.216  INFO 4124 --- [  restartedMain] com.example.demo.DemoApplication         : Started DemoApplication in 2.694 seconds (JVM running for 3.637)
```

今後はコンテナ内の/appで作業するものとする

### ping-pongコントローラー作成
1. PingController.javaを作成

2. ping-pongを確認
```
curl localhost:8080/ping
```

3. 「なぜこれで動いてまうの？？」の解説(DIコンテナとControllerアノテーションについて)

### 「生徒管理」の業務を実装する

1. 今回の仕様の説明
2. TODOを上から順々に完了させていく
