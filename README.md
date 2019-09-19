# SonarQube Maven POC
SonarQube, quality gates, profiles, maven plugin and docker

_bootstrap sonar_

```shell script
docker-compose up
# ...
# sonar_1  | 2019.09.19 17:56:03 INFO  app[][o.s.a.SchedulerImpl] Process[ce] is up
# sonar_1  | 2019.09.19 17:56:03 INFO  app[][o.s.a.SchedulerImpl] SonarQube is up
```

_do analysis_

```bash
./mvnw -f shitty-demo-project/pom.xml
```

_teardown_

```shell script
docker-compose down
# or cleanup: docker-compose down -v --rmi local
```

_links_

* [SonarQube docker image](https://hub.docker.com/_/sonarqube/)
* [SonarScanner for Maven](https://docs.sonarqube.org/latest/analysis/scan/sonarscanner-for-maven/)
* [SonarQube maven examples](https://github.com/SonarSource/sonar-scanning-examples/tree/master/sonarqube-scanner-maven)
