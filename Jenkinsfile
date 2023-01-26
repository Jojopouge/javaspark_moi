pipeline {
  agent any
  stages {
    stage('test') {
      parallel {
        stage('test windows') {
          steps {
            sh 'echo test'
          }
        }

        stage('ben deux') {
          steps {
            sh 'echo test linux'
          }
        }

      }
    }

    stage('verif') {
      steps {
        sh 'echo wesh wesh'
        sh 'ls -la'
        fileExists 'pom.xml'
      }
    }

    stage('build') {
      steps {
        sh 'mvn clean install'
      }
    }

    stage('Publish reports') {
      steps {
        sh 'echo qq chose'
      }
    }

    stage('Deploy') {
      steps {
        sh 'echo deploy'
      }
    }

  }
}