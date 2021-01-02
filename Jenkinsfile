library identifier: 'jenkins-shared-lib-demo1@master',
        retriever: modernSCM([$class: 'GitSCMSource',
         remote: 'https://github.com/hhammidd/jenkins-shared-lib-demo1.git'])

pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        doEcho()
        echo 'Hello $BUILD_NUMBER the DEMO is $DEMO'
      }
    }
    stage('goodbye') {
          steps {
            goodBye(' Hamid')
          }
        }

  }
  environment {
    DEMO = '1'
  }
}
