
CM Startup Log:

[root@instance-2 skanduri1987]# head -5 /var/log/cloudera-scm-server/cloudera-scm-server.log 
2018-05-17 07:39:02,847 INFO main:com.cloudera.server.cmf.Main: Starting SCM Server. JVM Args: [-Dlog4j.configuration=file:/etc/cloudera-scm-server/log4j.properties, -Dfile.encoding=UT
F-8, -Dcmf.root.logger=INFO,LOGFILE, -Dcmf.log.dir=/var/log/cloudera-scm-server, -Dcmf.log.file=cloudera-scm-server.log, -Dcmf.jetty.threshhold=WARN, -Dcmf.schema.dir=/usr/share/cmf/sc
hema, -Djava.awt.headless=true, -Djava.net.preferIPv4Stack=true, -Dpython.home=/usr/share/cmf/python, -XX:+UseConcMarkSweepGC, -XX:+UseParNewGC, -XX:+HeapDumpOnOutOfMemoryError, -Xmx2G
, -XX:MaxPermSize=256m, -XX:+HeapDumpOnOutOfMemoryError, -XX:HeapDumpPath=/tmp, -XX:OnOutOfMemoryError=kill -9 %p], Args: [], Version: 5.13.3 (#6 built by jenkins on 20180328-1830 git:
 f90c58536c252d70a23bde6d94514d92a1f111d4)
2018-05-17 07:39:02,939 INFO main:org.mortbay.log: Logging to org.slf4j.impl.Log4jLoggerAdapter(org.mortbay.log) via org.mortbay.log.Slf4jLog
2018-05-17 07:39:03,043 INFO main:org.springframework.context.support.ClassPathXmlApplicationContext: Refreshing org.springframework.context.support.ClassPathXmlApplicationContext@30a3
107a: startup date [Thu May 17 07:39:03 UTC 2018]; root of context hierarchy
2018-05-17 07:39:03,157 INFO main:org.springframework.beans.factory.xml.XmlBeanDefinitionReader: Loading XML bean definitions from class path resource [webapp/WEB-INF/spring/beanRefFac
tory.xml]
2018-05-17 07:39:03,602 INFO main:org.springframework.beans.factory.support.DefaultListableBeanFactory: Pre-instantiating singletons in org.springframework.beans.factory.support.Defaul
tListableBeanFactory@776aec5c: defining beans [bootstrapContext,rootContext]; root of factory hierarchy


JEtty server log:

2018-05-17 07:40:04,640 INFO WebServerImpl:org.mortbay.log: jetty-6.1.26.cloudera.4
2018-05-17 07:40:04,641 INFO WebServerImpl:org.mortbay.log: Started SelectChannelConnector@0.0.0.0:7180
2018-05-17 07:40:04,641 INFO WebServerImpl:com.cloudera.server.cmf.WebServerImpl: Started Jetty server.
2018-05-17 07:40:05,297 INFO ScmActive-0:com.cloudera.server.cmf.components.ScmActive: ScmActive completed successfully.
