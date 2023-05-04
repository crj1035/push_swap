pipeline {
  agent any
  stages {
    stage('Build')
    {
      steps {
        sh 'sudo apt-get install make -y'
      }
      steps {
        sh 'make push_swap'
      }
      steps {
        sh 'make checker'
      }
    }
    stage('Test')
    {
      steps {
        sh './push_swap 45 3 8 2 5 6 9 1 | ./checker 45 3 8 2 5 6 9 1'
      }
    }
  }
}
