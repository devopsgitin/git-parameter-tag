// pipeline {
//   agent any
//   stages {
//     stage('Example') {
//       steps {
//         checkout([
//           $class: 'GitSCM',
//           branches: [[name: '$tagname']],
//           userRemoteConfigs: [[url: 'https://github.com/devopsgitin/git-parameter-tag.git']]
//         ])
//         sh 'cat code.txt'
//       }
//     }
//   }
// }

pipeline {
  agent any
  stages {
    stage('Example') {
      steps {
        checkout scmGit(branches: [[name: '$tagname']], 
                        userRemoteConfigs: [[url: 'https://github.com/devopsgitin/git-parameter-tag.git']])
        sh 'cat code.txt'
      }
    }
  }
}
