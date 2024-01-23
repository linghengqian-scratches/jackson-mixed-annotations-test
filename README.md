# jackson-mixed-annotations-test

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
./mvnw clean test
[INFO] Scanning for projects...
[INFO] 
[INFO] --------------< com.lingh:jackson-mixed-annotations-test >--------------
[INFO] Building jackson-mixed-annotations-test 1.0-SNAPSHOT
[INFO]   from pom.xml
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- clean:3.2.0:clean (default-clean) @ jackson-mixed-annotations-test ---
[INFO] Deleting /home/linghengqian/TwinklingLiftWorks/git/public/jackson-mixed-annotations-test/target
[INFO] 
[INFO] --- resources:3.3.1:resources (default-resources) @ jackson-mixed-annotations-test ---
[INFO] skip non existing resourceDirectory /home/linghengqian/TwinklingLiftWorks/git/public/jackson-mixed-annotations-test/src/main/resources
[INFO] 
[INFO] --- compiler:3.11.0:compile (default-compile) @ jackson-mixed-annotations-test ---
[INFO] No sources to compile
[INFO] 
[INFO] --- resources:3.3.1:testResources (default-testResources) @ jackson-mixed-annotations-test ---
[INFO] skip non existing resourceDirectory /home/linghengqian/TwinklingLiftWorks/git/public/jackson-mixed-annotations-test/src/test/resources
[INFO] 
[INFO] --- compiler:3.11.0:testCompile (default-testCompile) @ jackson-mixed-annotations-test ---
[INFO] Changes detected - recompiling the module! :source
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
[ERROR] Tests run: 1, Failures: 1, Errors: 0, Skipped: 0, Time elapsed: 0.273 s <<< FAILURE! -- in com.lingh.RequiredTest
[ERROR] com.lingh.RequiredTest.assertRequiredValue -- Time elapsed: 0.243 s <<< FAILURE!
org.opentest4j.AssertionFailedError: 
Unexpected exception thrown: com.fasterxml.jackson.databind.exc.MismatchedInputException: Missing required creator property '' (index 0)
 at [Source: (StringReader); line: 4, column: 1] (through reference chain: com.lingh.RequiredTest$TestRecordWithoutLocalName[""])
        at org.junit.jupiter.api.AssertionFailureBuilder.build(AssertionFailureBuilder.java:152)
        at org.junit.jupiter.api.AssertDoesNotThrow.createAssertionFailedError(AssertDoesNotThrow.java:84)
        at org.junit.jupiter.api.AssertDoesNotThrow.assertDoesNotThrow(AssertDoesNotThrow.java:53)
        at org.junit.jupiter.api.AssertDoesNotThrow.assertDoesNotThrow(AssertDoesNotThrow.java:36)
        at org.junit.jupiter.api.Assertions.assertDoesNotThrow(Assertions.java:3168)
        at com.lingh.RequiredTest.assertRequiredValue(RequiredTest.java:26)
        at java.base/java.lang.reflect.Method.invoke(Method.java:580)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
        at java.base/java.util.ArrayList.forEach(ArrayList.java:1596)
Caused by: com.fasterxml.jackson.databind.exc.MismatchedInputException: Missing required creator property '' (index 0)
 at [Source: (StringReader); line: 4, column: 1] (through reference chain: com.lingh.RequiredTest$TestRecordWithoutLocalName[""])
        at com.fasterxml.jackson.databind.exc.MismatchedInputException.from(MismatchedInputException.java:59)
        at com.fasterxml.jackson.databind.DeserializationContext.reportInputMismatch(DeserializationContext.java:1781)
        at com.fasterxml.jackson.databind.deser.impl.PropertyValueBuffer._findMissing(PropertyValueBuffer.java:192)
        at com.fasterxml.jackson.databind.deser.impl.PropertyValueBuffer.getParameters(PropertyValueBuffer.java:158)
        at com.fasterxml.jackson.databind.deser.ValueInstantiator.createFromObjectWith(ValueInstantiator.java:301)
        at com.fasterxml.jackson.databind.deser.impl.PropertyBasedCreator.build(PropertyBasedCreator.java:202)
        at com.fasterxml.jackson.databind.deser.BeanDeserializer._deserializeUsingPropertyBased(BeanDeserializer.java:526)
        at com.fasterxml.jackson.databind.deser.BeanDeserializerBase.deserializeFromObjectUsingNonDefault(BeanDeserializerBase.java:1493)
        at com.fasterxml.jackson.databind.deser.BeanDeserializer.deserializeFromObject(BeanDeserializer.java:348)
        at com.fasterxml.jackson.databind.deser.BeanDeserializer.deserialize(BeanDeserializer.java:185)
        at com.fasterxml.jackson.dataformat.xml.deser.XmlDeserializationContext.readRootValue(XmlDeserializationContext.java:104)
        at com.fasterxml.jackson.databind.ObjectMapper._readMapAndClose(ObjectMapper.java:4899)
        at com.fasterxml.jackson.databind.ObjectMapper.readValue(ObjectMapper.java:3846)
        at com.fasterxml.jackson.databind.ObjectMapper.readValue(ObjectMapper.java:3814)
        at com.lingh.RequiredTest.lambda$assertRequiredValue$1(RequiredTest.java:27)
        at org.junit.jupiter.api.AssertDoesNotThrow.assertDoesNotThrow(AssertDoesNotThrow.java:49)
        ... 6 more

[INFO] 
[INFO] Results:
[INFO] 
[ERROR] Failures: 
[ERROR]   RequiredTest.assertRequiredValue:26 Unexpected exception thrown: com.fasterxml.jackson.databind.exc.MismatchedInputException: Missing required creator property '' (index 0)
 at [Source: (StringReader); line: 4, column: 1] (through reference chain: com.lingh.RequiredTest$TestRecordWithoutLocalName[""])
[INFO] 
[ERROR] Tests run: 1, Failures: 1, Errors: 0, Skipped: 0
[INFO] 
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  3.020 s
[INFO] Finished at: 2024-01-23T18:52:29+08:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-surefire-plugin:3.2.2:test (default-test) on project jackson-mixed-annotations-test: There are test failures.
[ERROR] 
[ERROR] Please refer to /home/linghengqian/TwinklingLiftWorks/git/public/jackson-mixed-annotations-test/target/surefire-reports for the individual test results.
[ERROR] Please refer to dump files (if any exist) [date].dump, [date]-jvmRun[N].dump and [date].dumpstream.
[ERROR] -> [Help 1]
[ERROR] 
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR] 
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoFailureException
```