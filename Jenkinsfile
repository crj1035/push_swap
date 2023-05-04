pipeline {
  agent any
  stages {
      stage('Compilation de push_swap')
      {
          steps {
              sh 'make push_swap'       
          }
      }
      stage('Compilation de checker')
      {
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
