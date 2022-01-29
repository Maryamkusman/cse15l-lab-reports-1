# CSE15L Lab Report 2
## Code Change #1

> **code change diff from Github**
![Image](https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/Screen%20Shot%202022-01-28%20at%207.11.40%20PM.png)

> **The link of failure-inducing input**
[image.md](https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/image.md)

> **symptom of failure-inducing inputs after running main**
![symptom of main](https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/Screen%20Shot%202022-01-28%20at%207.40.21%20PM.png)
```

xiaolongdeMBP:markdown-parse xiaolong$  java MarkdownParse image.md  
[https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/Screen%20Shot%202022-01-12%20at%2011.13.50%20PM.png]

```
> **symptom of failure-inducing inputs after running JUnit Test**
![symptom of Junit](https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/Screen%20Shot%202022-01-28%20at%208.44.30%20PM.png)

```
xiaolongdeMBP:markdown-parse xiaolong$ javac -cp .:lib/junit-4.12.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java            xiaolongdeMBP:markdown-parse xiaolong$ java -cp .:lib/junit-4.12.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest
JUnit version 4.12
.E..
Time: 0.02
There was 1 failure:
1) testNew(MarkdownParseTest)
java.lang.AssertionError: expected:<[]> but was:<[https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/Screen%20Shot%202022-01-12%20at%2011.13.50%20PM.png]>
        at org.junit.Assert.fail(Assert.java:88)
        at org.junit.Assert.failNotEquals(Assert.java:834)
        at org.junit.Assert.assertEquals(Assert.java:118)
        at org.junit.Assert.assertEquals(Assert.java:144)
        at MarkdownParseTest.testNew(MarkdownParseTest.java:23)
        at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
        at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.base/java.lang.reflect.Method.invoke(Method.java:564)
        at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:50)
        at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
        at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:47)
        at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
        at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:325)
        at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:78)
        at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:57)
        at org.junit.runners.ParentRunner$3.run(ParentRunner.java:290)
        at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:71)
        at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:288)
        at org.junit.runners.ParentRunner.access$000(ParentRunner.java:58)
        at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:268)
        at org.junit.runners.ParentRunner.run(ParentRunner.java:363)
        at org.junit.runners.Suite.runChild(Suite.java:128)
        at org.junit.runners.Suite.runChild(Suite.java:27)
        at org.junit.runners.ParentRunner$3.run(ParentRunner.java:290)
        at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:71)
        at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:288)
        at org.junit.runners.ParentRunner.access$000(ParentRunner.java:58)
        at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:268)
        at org.junit.runners.ParentRunner.run(ParentRunner.java:363)
        at org.junit.runner.JUnitCore.run(JUnitCore.java:137)
        at org.junit.runner.JUnitCore.run(JUnitCore.java:115)
        at org.junit.runner.JUnitCore.runMain(JUnitCore.java:77)
        at org.junit.runner.JUnitCore.main(JUnitCore.java:36)
```

> **relationship between the bug, the symptom, and the failure-inducing input**







## Code Change #2
> **code change diff from Github**
![Image](https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/Screen%20Shot%202022-01-29%20at%2012.19.36%20AM.png)

> **The link of failure-inducing input**
[invalidlink.md](https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/invalidlink.md)

> **symptom of failure-inducing inputs after running main**
![symptom of main](https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/Screen%20Shot%202022-01-28%20at%2010.55.47%20PM.png)
```

xiaolongdeMBP:markdown-parse xiaolong$ javac MarkdownParse.java 
xiaolongdeMBP:markdown-parse xiaolong$  java MarkdownParse invalidlink.md
[https://something.png, https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/Screen%20Shot%202022-01-12%20at%2011.13.50%20PM.png]
xiaolongdeMBP:markdown-parse xiaolong$ 

```
> **symptom of failure-inducing inputs after running JUnit Test**
![symptom of Junit](https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/Screen%20Shot%202022-01-28%20at%2010.48.44%20PM.png)

```
xiaolongdeMBP:markdown-parse xiaolong$ javac -cp .:lib/junit-4.12.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.javaxiaolongdeMBP:markdown-parse xiaolong$ java -cp .:lib/junit-4.12.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest
JUnit version 4.12
.E...
Time: 0.02
There was 1 failure:
1) testInvalidlink(MarkdownParseTest)
java.lang.AssertionError: expected:<[]> but was:<[https://something.png, https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/Screen%20Shot%202022-01-12%20at%2011.13.50%20PM.png]>
        at org.junit.Assert.fail(Assert.java:88)
        at org.junit.Assert.failNotEquals(Assert.java:834)
        at org.junit.Assert.assertEquals(Assert.java:118)
        at org.junit.Assert.assertEquals(Assert.java:144)
        at MarkdownParseTest.testInvalidlink(MarkdownParseTest.java:29)
        at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
        at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.base/java.lang.reflect.Method.invoke(Method.java:564)
        at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:50)
        at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
        at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:47)
        at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
        at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:325)
        at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:78)
        at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:57)
        at org.junit.runners.ParentRunner$3.run(ParentRunner.java:290)
        at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:71)
        at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:288)
        at org.junit.runners.ParentRunner.access$000(ParentRunner.java:58)
        at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:268)
        at org.junit.runners.ParentRunner.run(ParentRunner.java:363)
        at org.junit.runners.Suite.runChild(Suite.java:128)
        at org.junit.runners.Suite.runChild(Suite.java:27)
        at org.junit.runners.ParentRunner$3.run(ParentRunner.java:290)
        at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:71)
        at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:288)
        at org.junit.runners.ParentRunner.access$000(ParentRunner.java:58)
        at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:268)
        at org.junit.runners.ParentRunner.run(ParentRunner.java:363)
        at org.junit.runner.JUnitCore.run(JUnitCore.java:137)
        at org.junit.runner.JUnitCore.run(JUnitCore.java:115)
        at org.junit.runner.JUnitCore.runMain(JUnitCore.java:77)
        at org.junit.runner.JUnitCore.main(JUnitCore.java:36)
```

> **relationship between the bug, the symptom, and the failure-inducing input**







## Code Change #3

> **code change diff from Github**
![Image](https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/Screen%20Shot%202022-01-29%20at%2012.22.52%20AM.png)

> **The link of failure-inducing input**
[whatever.md](https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/whatever.md)

> **symptom of failure-inducing inputs after running main**
![symptom of main](https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/Screen%20Shot%202022-01-29%20at%2012.26.11%20AM.png)
```

xiaolongdeMBP:markdown-parse xiaolong$  java MarkdownParse whatever.md
[somehow.com, abc.com]

```
> **symptom of failure-inducing inputs after running JUnit Test**
![symptom of Junit](https://github.com/KristinShuyiHan/cse15l-lab-reports/blob/main/Screen%20Shot%202022-01-29%20at%2012.20.13%20AM.png)

```
xiaolongdeMBP:markdown-parse xiaolong$ javac -cp .:lib/junit-4.12.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.javaxiaolongdeMBP:markdown-parse xiaolong$ java -cp .:lib/junit-4.12.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest
JUnit version 4.12
.E....
Time: 0.023
There was 1 failure:
1) testWhatever(MarkdownParseTest)
java.lang.AssertionError: expected:<[abc.com]> but was:<[somehow.com, abc.com]>
        at org.junit.Assert.fail(Assert.java:88)
        at org.junit.Assert.failNotEquals(Assert.java:834)
        at org.junit.Assert.assertEquals(Assert.java:118)
        at org.junit.Assert.assertEquals(Assert.java:144)
        at MarkdownParseTest.testWhatever(MarkdownParseTest.java:35)
        at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
        at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.base/java.lang.reflect.Method.invoke(Method.java:564)
        at org.junit.runners.model.FrameworkMethod$1.runReflectiveCall(FrameworkMethod.java:50)
        at org.junit.internal.runners.model.ReflectiveCallable.run(ReflectiveCallable.java:12)
        at org.junit.runners.model.FrameworkMethod.invokeExplosively(FrameworkMethod.java:47)
        at org.junit.internal.runners.statements.InvokeMethod.evaluate(InvokeMethod.java:17)
        at org.junit.runners.ParentRunner.runLeaf(ParentRunner.java:325)
        at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:78)
        at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:57)
        at org.junit.runners.ParentRunner$3.run(ParentRunner.java:290)
        at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:71)
        at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:288)
        at org.junit.runners.ParentRunner.access$000(ParentRunner.java:58)
        at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:268)
        at org.junit.runners.ParentRunner.run(ParentRunner.java:363)
        at org.junit.runners.Suite.runChild(Suite.java:128)
        at org.junit.runners.Suite.runChild(Suite.java:27)
        at org.junit.runners.ParentRunner$3.run(ParentRunner.java:290)
        at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:71)
        at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:288)
        at org.junit.runners.ParentRunner.access$000(ParentRunner.java:58)
        at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:268)
        at org.junit.runners.ParentRunner.run(ParentRunner.java:363)
        at org.junit.runner.JUnitCore.run(JUnitCore.java:137)
        at org.junit.runner.JUnitCore.run(JUnitCore.java:115)
        at org.junit.runner.JUnitCore.runMain(JUnitCore.java:77)
        at org.junit.runner.JUnitCore.main(JUnitCore.java:36)

FAILURES!!!
Tests run: 5,  Failures: 1
```

> **relationship between the bug, the symptom, and the failure-inducing input**
