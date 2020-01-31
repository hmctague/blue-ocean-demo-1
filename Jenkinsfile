pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'I am building some code!'
        sh 'cat /etc/hosts'
        sh 'cat README.md'
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
