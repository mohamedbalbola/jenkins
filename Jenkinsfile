pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'we are building the code and will be ready for deployment '
      }
    }

    stage('test') {
      steps {
        sh '''python3 --version 
echo "name is mohamed balboula"'''
      }
    }

    stage('final ') {
      steps {
        sh 'echo "build and test were successfully done and this is a success message"'
      }
    }

    stage('test-envcar') {
      agent any
      environment {
        message_printed = 'this job was powerfully over'
      }
      steps {
        echo "this pipeline is bringing us ${message_printed}"
      }
    }

    stage('test if app is ready for prod') {
      steps {
        input 'do you want to deploy this to production?'
      }
    }

  }
}