pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        echo 'Hello $BUILD_NUMBER the DEMO is $DEMO'
      }
    }

  }
  environment {
    DEMO = '1'
  }
}