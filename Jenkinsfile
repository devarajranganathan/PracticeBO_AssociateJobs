pipeline {
  agent any
  stages {
    stage('JobA') {
      steps {
        parallel(
          "JobA": {
            node(label: 'Master') {
              build 'MultiJob_Jobs/A'
            }
            
            
          },
          "JobB": {
            node(label: 'Sid_Machine') {
              build 'MultiJob_Jobs/B'
            }
            
            
          }
        )
      }
    }
    stage('JobC') {
      steps {
        node(label: 'Master') {
          build 'MultiJob_Jobs/C'
        }
        
      }
    }
  }
}