pipeline {
  agent any
  stages {
    stage('Example') {
      steps {
        checkout([
          $class: 'GitSCM',
          branches: [[name: '$tagname']],
          extension: [],
          userRemoteConfigs: [[url: 'https://github.com/devopsgitin/git-parameter-tag.git']]
        ])
        sh 'cat code.txt'
      }
    }
  }
}
