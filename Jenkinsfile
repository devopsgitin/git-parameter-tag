pipeline {
    agent any
    parameters {
        gitParameter name: 'BRANCH_TAG',
                     type: 'PT_BRANCH_TAG',
                     defaultValue: 'main'
    }
    stages {
        stage ("JOB") {
            steps {
                checkout ([
                    $class: 'GitSCM',
                    branches: [[name: '${params.BRANCH_TAG}']],
                    extensions: [],
                    userRemoteConfigs: [[url: 'https://github.com/devopsgitin/git-parameter-tag.git']]
                ])
                sh 'cat code.txt'
            }
        }
    }
}
