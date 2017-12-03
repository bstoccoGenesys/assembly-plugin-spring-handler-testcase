Forked from https://github.com/cjrequena/samples.git to test assembly-plugin with spring

To test, switch between "assembly-plugin" and "main" branches, do `mvn clean package` and examine spring.handlers contents:

```bash
$ unzip -p target/OTV_Spring_ThreadPool-0.0.1-SNAPSHOT.jar META-INF/spring.handlers
http\://www.springframework.org/schema/context=org.springframework.context.config.ContextNamespaceHandler
http\://www.springframework.org/schema/jee=org.springframework.ejb.config.JeeNamespaceHandler
http\://www.springframework.org/schema/lang=org.springframework.scripting.config.LangNamespaceHandler
http\://www.springframework.org/schema/task=org.springframework.scheduling.config.TaskNamespaceHandler

http\://www.springframework.org/schema/aop=org.springframework.aop.config.AopNamespaceHandler

http\://www.springframework.org/schema/p=org.springframework.beans.factory.xml.SimplePropertyNamespaceHandler
http\://www.springframework.org/schema/util=org.springframework.beans.factory.xml.UtilNamespaceHandler

http\://www.springframework.org/schema/tx=org.springframework.transaction.config.TxNamespaceHandler

$ unzip -p target/OTV_Spring_ThreadPool-0.0.1-SNAPSHOT-jar-with-dependencies.jar META-INF/spring.handlers
http\://www.springframework.org/schema/context=org.springframework.context.config.ContextNamespaceHandler
http\://www.springframework.org/schema/jee=org.springframework.ejb.config.JeeNamespaceHandler
http\://www.springframework.org/schema/lang=org.springframework.scripting.config.LangNamespaceHandler
http\://www.springframework.org/schema/task=org.springframework.scheduling.config.TaskNamespaceHandler
```
