pipeline {
  agent any
  stages {
    stage('BuildTest') {
      parallel {
        stage('Build') {
          steps {
            echo 'Build .NET core application'
          }
        }

        stage('Test') {
          steps {
            echo 'Testing the application'
            echo "Chrome Driver Path is ${ChromeDriverPath}"
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying the app in IIS server'
      }
    }

  }
  environment {
    ChromeDriverPath = 'C:\\ChanPath'
  }
}
