pipeline {
  agent any
  stages {
    stage('Development Build') {
      steps {
        echo 'Pull the code from git hub repo'
        echo 'Create a Build using Repository'
      }
    }

    stage('Smoke Test') {
      steps {
        echo 'Run two smoke test'
      }
    }

    stage('Deploy in QA Envrionment') {
      steps {
        echo 'Stop the Server'
        echo 'Move the build in QA'
        echo 'Start the Server in QA'
        echo 'Notify to QA by Email'
      }
    }

    stage('Integration Test') {
      parallel {
        stage('Integration Test') {
          steps {
            echo 'UI Based Testing'
          }
        }

        stage('API Testing') {
          steps {
            echo 'Run Rest Automation Tests'
          }
        }

        stage('Performance Testing') {
          steps {
            echo 'Run Jmeter Tests'
          }
        }

      }
    }

    stage('Certify') {
      steps {
        echo 'QA team Certify'
      }
    }

  }
}