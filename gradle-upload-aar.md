如何上传aar到maven仓库
==

* 复制 `gradle-mvn-push.gradle`到当前的项目空间中
* 在 `build.gradle` 中添加 `apply from: './gradle-mvn-push.gradle'`
* 配置相配置如下

  ```
  POM_NAME= name
  VERSION_NAME=版本号
  VERSION_CODE=版本代码
  GROUP= group
  POM_ARTIFACT_ID= artifact id
  POM_PACKAGING=aar 
  RELEASE_REPOSITORY_URL=nexus release地址
  SNAPSHOT_REPOSITORY_URL=nexus snapshots地址

  NEXUS_USERNAME=nexus账号
  NEXUS_PASSWORD=nexus 密码
  ```
  
* 运行 `$ gradle clean build uploadArchives`


