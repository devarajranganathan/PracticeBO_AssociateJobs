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
            node(label: 'Master') {
              build 'MultiJob_Jobs/B'
            }
            
            
          }
        )
      }
    }
    stage('JobC') {
      steps {
        parallel(
          "JobC": {
            node(label: 'Sid_Machine') {
              build 'MultiJob_Jobs/C'
            }
            
            
          },
          "JobD": {
            node(label: 'Sid_Machine') {
              build 'MultiJob_Jobs/D'
            }
            
            
          }
        )
      }
    }
  }
}