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
        sh '''git clone https://github.com/sbhal/test_jenkins.git
        echo "test1" >> README.md
        
        if [[ `git status --porcelain` ]]; then
        echo Something to commit
        git diff --no-pager
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
