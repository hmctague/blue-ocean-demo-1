pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'I am building some code!'
        ws(dir: 'foo1') {
          echo 'dfgtdfg'
        }
        
        node(label: 'bar1') {
          git(url: 'file:///space/mctague/tstrepos/blue-ocean-demo-3', poll: true, changelog: true)
        }
        
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
        parallel(
          "Deploy": {
            echo 'Ship It!'
            
          },
          "Win": {
            bat 'h2'
            
          }
        )
      }
    }
  }
}