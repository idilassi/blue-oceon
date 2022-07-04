pipeline {
  agent any
  stages {
    stage('build stages') {
      steps {
        echo 'build completed'
      }
    }

    stage('test stages') {
      parallel {
        stage('test2') {
          steps {
            echo 'running2'
          }
        }

        stage('test1') {
          steps {
            echo 'running test1'
          }
        }

      }
    }

    stage('deploy stages') {
      steps {
        echo 'deployment completed'
      }
    }

  }
}