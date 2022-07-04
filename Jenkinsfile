pipeline {
  agent any
  stages {
    stage('build stages') {
      steps {
        echo ' build good'
        retry(count: 3) {
          sh 'yooo'
        }

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
        input(message: 'u are sure to deplay', ok: 'yes im')
        echo 'deployment completed'
      }
    }

    stage('notiy for new build') {
      steps {
        echo 'new build ccompleted successfully'
      }
    }

  }
}