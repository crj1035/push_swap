pipeline {
  agent any
  stages {
    stage('Compilation du push_swap en C à l\'aide de make')
    {
      steps {
        sh 'make push_swap'
      }
    }
    stage('Compilation du checker en C à l\'aide de make')
    {
      steps {
        sh 'make checker'
      }
    }
  }
}
