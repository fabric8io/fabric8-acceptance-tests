# fabric8 acceptance tests

Automated testing using Serenity BDD and Selenium to perform acceptance test both in and outside of a CD pipeline.

## To Run locally..

First login into your openshift instance so that kuberentes-client is able to connect and assert behaviour server side.

```
oc login ux.fabric8.io --username=admin --password=admin
```

Next run the Serenity test suite optionally passing a target OpenShift API server..

```
mvn clean test -Dwebdriver.chrome.driver=chromedriver -Durl=http://fabric8.test.ux.fabric8.io
```