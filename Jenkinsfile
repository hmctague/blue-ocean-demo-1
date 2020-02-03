pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'I am building some code!'
        sh 'cat /etc/hosts'
        sh 'cat README.md'
        sh 'pv -L 30k -q build-20200129210503.log'

        // This displays colors using the 'xterm' ansi color map.
        ansiColor('xterm') {
            // Just some echoes to show the ANSI color.
            echo "\u001B[31mI'm Red\u001B[0m Now not"
        }

      }
    }
    stage('Test1') {
      steps {
        echo 'Ship It!'
      }
    }
    stage('This is a really long stage name') {
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
