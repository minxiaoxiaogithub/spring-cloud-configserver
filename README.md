# spring-cloud-configserver
1.添加spring-cloud-config服务端包依赖
<dependency>
	<groupId>org.springframework.cloud</groupId>
	<artifactId>spring-cloud-config-server</artifactId>
</dependency>

2.启动类添加@EnableConfigServer注解
@EnableConfigServer
@SpringBootApplication
public class ConfigserverApplication {

	public static void main(String[] args) {
		SpringApplication.run(ConfigserverApplication.class, args);
	}

}

3.修改配置文件
#端口
server.port=8888
#应用名
spring.application.name=configserver


#从本地获取配置文件
#spring.profiles.active=native
#文件路径
#spring.cloud.config.server.native.searchLocations=file:C:/fiberhome/xx_work_pro/self_study/configserver


#配置git仓库地址
spring.cloud.config.server.git.uri=https://github.com/minxiaoxiaogithub/tes-config
#配置文件所在目录
spring.cloud.config.server.git.search-paths=/**
#配置仓库的分支
spring.cloud.config.label=master
#访问git仓库的用户名
#spring.cloud.config.server.git.username=admin
#访问git仓库的用户密码 如果Git仓库为公开仓库，可以不填写用户名和密码，如果是私有仓库需要填写
#spring.cloud.config.server.git.password=123456
