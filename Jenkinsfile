pipeline {
  agent any
  stages {
    stage('JobA') {
      steps {
        parallel(
          "JobA": {
            build 'MultiJob_Jobs/A'
            
          },
          "JobB": {
            build 'MultiJob_jobs/B'
            
          }
        )
      }
    }
    stage('JobC') {
      steps {
        parallel(
          "JobC": {
            build 'MultiJob_Jobs/C'
            
          },
          "JobD": {
            build 'MultiJob_Jobs/D'
            
          }
        )
      }
    }
  }
}