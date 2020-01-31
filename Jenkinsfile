pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'I am building some code!'
        sh 'cat /etc/hosts'
        sh 'cat README.md'
        sh 'pv -L 30k -q build-20200129210503.log'
      }
    }
    stage('Test1') {
      steps {
        echo 'Ship It!'
      }
    }
    stage('Test2') {
      steps {
        echo 'Ship It!'
      }
    }
    stage('Test3') {
      steps {
        echo 'Ship It!'
      }
    }
    stage('Test4') {
      steps {
        echo 'Ship It!'
      }
    }
    stage('This is a really long stage name') {
      steps {
        echo 'Ship It!'
      }
    }
    stage('Test5') {
      steps {
        echo 'Ship It!'
      }
    }
    stage('Test6') {
      steps {
        echo 'Ship It!'
      }
    }
    stage('Test7') {
      steps {
        echo 'Ship It!'
      }
    }
    stage('Test8') {
      steps {
        echo 'Ship It!'
      }
    }
    stage('Test') {
      steps {
        parallel(
          "Unit Tests": {
            echo 'Unit Tests Are Awesome!'
            
          },
          "Integration Tests": {
            echo 'Integration Tests Are Awesome!'
            
          },
          "Smoke Tests": {
            echo 'Where There is Smoke there is Fire!!!'
            
          }
        )
      }
    }
    stage('Deploy') {
      steps {
        echo 'Ship It!'
      }
    }
  }
}
