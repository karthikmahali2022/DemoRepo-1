pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn compile'
      }
    }

    stage('Email') {
      steps {
        emailext(subject: 'Build status', attachLog: true, body: 'Build log', from: 'karthikmahali@gmail.com', to: 'karthikmahali@gmail.com')
      }
    }

  }
}