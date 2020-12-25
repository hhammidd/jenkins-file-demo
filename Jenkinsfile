pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        doSh()
        echo 'Hello $BUILD_NUMBER the DEMO is $DEMO'
      }
    }

  }
  environment {
    DEMO = '1'
  }
}

 void doSh() {
    sh 'echo "Hello babe $BUILD_NUMBER the DEMO is $DEMO"'
  }