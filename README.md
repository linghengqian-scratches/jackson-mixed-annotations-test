# jackson-mixed-annotations-test

- For https://github.com/FasterXML/jackson-dataformat-xml/issues/628 .

- Execute the following command on the Ubuntu 22.04.3 instance with `SDKMAN!` installed.

```shell
sdk install java 21.0.2-graalce
sdk use java 21.0.2-graalce

git clone git@github.com:linghengqian/jackson-mixed-annotations-test.git
cd ./jackson-mixed-annotations-test/
./mvnw clean test
```

- Log.
```shell
$ ./mvnw clean test
[INFO] Scanning for projects...
[INFO] 
[INFO] --------------< com.lingh:jackson-mixed-annotations-test >--------------
[INFO] Building jackson-mixed-annotations-test 1.0-SNAPSHOT
[INFO]   from pom.xml
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- clean:3.2.0:clean (default-clean) @ jackson-mixed-annotations-test ---
[INFO] 
[INFO] --- resources:3.3.1:resources (default-resources) @ jackson-mixed-annotations-test ---
[INFO] skip non existing resourceDirectory /home/linghengqian/TwinklingLiftWorks/git/public/jackson-mixed-annotations-test/src/main/resources
[INFO] 
[INFO] --- compiler:3.12.1:compile (default-compile) @ jackson-mixed-annotations-test ---
[INFO] No sources to compile
[INFO] 
[INFO] --- resources:3.3.1:testResources (default-testResources) @ jackson-mixed-annotations-test ---
[INFO] skip non existing resourceDirectory /home/linghengqian/TwinklingLiftWorks/git/public/jackson-mixed-annotations-test/src/test/resources
[INFO] 
[INFO] --- compiler:3.12.1:testCompile (default-testCompile) @ jackson-mixed-annotations-test ---
[INFO] Recompiling the module because of changed source code.
[INFO] Compiling 1 source file with javac [debug target 21] to target/test-classes
[INFO] 由于在类路径中发现了一个或多个处理程序，因此启用了
  批注处理。未来发行版的 javac 可能会禁用批注处理，
  除非至少按名称指定了一个处理程序 (-processor)，
  或指定了搜索路径 (--processor-path, --processor-module-path)，
  或显式启用了批注处理 (-proc:only, -proc:full)。
  可使用 -Xlint:-options 隐藏此消息。
  可使用 -proc:none 禁用批注处理。
[INFO] 
[INFO] --- surefire:3.2.2:test (default-test) @ jackson-mixed-annotations-test ---
[INFO] Using auto detected provider org.apache.maven.surefire.junitplatform.JUnitPlatformProvider
[INFO] 
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running com.lingh.RequiredTest
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.170 s -- in com.lingh.RequiredTest
[INFO] 
[INFO] Results:
[INFO] 
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0
[INFO] 
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  2.065 s
[INFO] Finished at: 2024-02-05T12:04:46+08:00
[INFO] ------------------------------------------------------------------------
```