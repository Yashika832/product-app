<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>2.5.3</version>
		<relativePath /> <!-- lookup parent from repository -->
	</parent>
	<groupId>product-app</groupId>
	<artifactId>product-app</artifactId>
	<version>0.0.1-SNAPSHOT</version>
	<name>product-app</name>
	<packaging>war</packaging>
	<description>Demo project for Spring Boot</description>
	<properties>
		<java.version>1.8</java.version>
		<surefire.version>2.17</surefire.version>
		<thucydides.version>1.8.4</thucydides.version>
		<jetty.port>9090</jetty.port>
		<jetty.stop.port>9999</jetty.stop.port>
	</properties>

	<distributionManagement>
		<repository>
			<id>release</id>
			<name>releases</name>
			<url>http://localhost:8081/artifactory/libs-release-local</url>
		</repository>
		<snapshotRepository>
			<id>snapshot</id>
			<name>snapshots</name>
			<url>http://localhost:8081/artifactory/libs-snapshot-local</url>
		</snapshotRepository>
	</distributionManagement>

	<scm>
		<connection>scm:git:git@github.com:Yashika832/product-app.git</connection>
		<developerConnection>scm:git:git@github.com:Yashika832/product-app.git</developerConnection>
		<url>git@github.com:Yashika832/product-app.git</url>
		<tag>v0.0.1</tag>
	</scm>


	<dependencies>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-actuator</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-jpa</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-validation</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
			<exclusions>
				<exclusion>
					<groupId>org.springframework.boot</groupId>
					<artifactId>spring-boot-starter-tomcat</artifactId>
				</exclusion>
			</exclusions>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-jetty</artifactId>
			<scope>provided</scope>
		</dependency>

		<!-- <dependency> <groupId>javax.servlet</groupId> <artifactId>javax.servlet-api</artifactId> 
			<scope>provided</scope> </dependency> -->

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-devtools</artifactId>
			<scope>runtime</scope>
			<optional>true</optional>
		</dependency>
		<dependency>
			<groupId>mysql</groupId>
			<artifactId>mysql-connector-java</artifactId>
			<scope>runtime</scope>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency>
	</dependencies>

	<build>
		<plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
			</plugin>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-release-plugin</artifactId>
				<version>3.0.0-M1</version>
				<configuration>
					<tagNameFormat>v@{project.version}</tagNameFormat>
					<autoVersionSubmodules>true</autoVersionSubmodules>
				</configuration>
			</plugin>

			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-surefire-plugin</artifactId>
			</plugin>


			<plugin>
				<groupId>org.jacoco</groupId>
				<artifactId>jacoco-maven-plugin</artifactId>
				<version>0.8.6</version>
				<executions>
					<execution>
						<id>default-prepare-agent</id>
						<goals>
							<goal>prepare-agent</goal>
						</goals>
					</execution>
					<execution>
						<id>default-report</id>
						<goals>
							<goal>report</goal>
						</goals>
					</execution>
					<execution>
						<id>default-check</id>
						<goals>
							<goal>check</goal>
						</goals>
						<configuration>
							<rules>
								<rule>
									<element>BUNDLE</element>
									<limits>
										<limit>
											<counter>COMPLEXITY</counter>
											<value>COVEREDRATIO</value>
											<minimum>0.20</minimum>
										</limit>
									</limits>
								</rule>
							</rules>
						</configuration>
					</execution>
				</executions>
				<configuration>
					<excludes>
						<exclude>com/eldisol/jacoboot/JacobootApplication.class</exclude>
					</excludes>
				</configuration>
			</plugin>


		</plugins>
	</build>

</project>