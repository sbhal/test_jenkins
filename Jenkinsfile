pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        echo 'This is test pipeline!'
      }
    }
    stage('stage2') {
      steps {
        sh '''if [[ `git status --porcelain` ]]; then
        echo Something to commit
else
        echo Nothing to commit
fi
'''
        sh '''git status
'''
        echo 'Done'
      }
    }
  }
}