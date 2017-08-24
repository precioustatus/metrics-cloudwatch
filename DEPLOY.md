### Why
This project is not active. There are several dependencies that prevent us from updating to newer versions of direct dependencies (AWS SDKs, for instance). So, until find a more active project (or write our own), we periodically update the dependencies of this project, build and deploy to our internal Maven repository.

### To Deploy (PreciouStatus)
1. Build
   - `./gradlew clean build`
2. Deploy
   - ```
   ./gradlew \
   -PdeployUrl=http://artifactory.precioustatus.net:8081/artifactory/libs-release-local \
   -PdeployUsername=<<username>> \
   -PdeployPassword=<<password>> \
   uploadArchives
```
