pipeline {
  agent any
  stages {
      stage('Compilation de push_swap')
      {
          steps {
              sh 'export TERM=xterm;make push_swap'       
          }
      }
      stage('Compilation de checker')
      {
          steps {
              sh 'export TERM=xterm;make checker'
          }
      }
      stage('Test 1')
      {
          steps {
              sh './push_swap 45 3 8 2 5 6 9 1 | ./checker 45 3 8 2 5 6 9 1'
          }
      }
      stage('Test 2')
      {
          steps {
              sh './push_swap 45 3 8 2 5 6 9 1 | ./checker 85 3 8 9 5 6 9 1'
          }
      }
   }
}
