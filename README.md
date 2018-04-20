# redissession-1.8
适用于JDK1.8 tomcat 8
tomcat根目录中的conf/context.xml配置信息：

<?xml version="1.0" encoding="UTF-8"?>
<Context>
    <WatchedResource>WEB-INF/web.xml</WatchedResource>
    <WatchedResource>${catalina.base}/conf/web.xml</WatchedResource>
<Manager className="com.redissesson.tomcat.redisson.ElasticacheSessionManager"
      <!-- 多个的配置方式 nodes="redis://192.168.1.170:6387 redis://192.168.1.170:6388"-->
        nodes="redis://192.168.1.170:6387" 
        nodePollInterval="1000"
        sessionKeyPrefix="_rsm_"
        saveOnChange="false"
        forceSaveAfterRequest="false"
        dirtyOnMutation="false"
        ignorePattern=".*\\.(ico|png|gif|jpg|jpeg|swf|css|js)$"
        maxSessionAttributeSize="-1"
        maxSessionSize="-1"
        allowOversizedSessions="false"
        masterConnectionPoolSize="100"
        slaveConnectionPoolSize="100"
        database="0"
        password="yangfuren"
        timeout="60000"
        pingTimeout="1000"
        retryAttempts="20"
        retryInterval="1000"
/>
</Context>


tomcat8下的jar下载地址：
https://download.csdn.net/download/github_38924695/10362489 下载后直接放入tomcat根目录下的lib中
