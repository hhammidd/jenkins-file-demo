* Create a separated folder
* 1. First create JenkinsFile
```
pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        doEcho()
        echo 'Hello $BUILD_NUMBER the DEMO is $DEMO'
      }
    }

  }
  environment {
    DEMO = '1'
  }
}
```
* 2. In JenkinsFile you need call a shared method (`doEcho()`) in `https://github.com/hhammidd/jenkins-shared-lib-demo1.git` 
* 3. Add the shared library info in jenkinsfile 
```
library identifier: 'jenkins-shared-lib-demo1@master',
        retriever: modernSCM([$class: 'GitSCMSource',
         remote: 'https://github.com/hhammidd/jenkins-shared-lib-demo1.git'])
```
* 4. create the pipline in Jenkins