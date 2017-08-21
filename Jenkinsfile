pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'I am building some code!'
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
            
          },
          "win": {
            bat 'tst1'
            
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