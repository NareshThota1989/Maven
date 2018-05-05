pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        git(url: 'https://github.com/NareshThota1989/Maven', branch: 'master')
      }
    }
    stage('Build') {
      steps {
        sh 'mvn clean compile package install'
      }
    }
    stage('Deploy') {
      steps {
        sh 'mvn deploy'
      }
    }
  }
}