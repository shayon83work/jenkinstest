pipeline {
  agent any
  parameters {
    string(name: 'branch', defaultValue: '', description: 'blah')
  }
  stages {
    stage('run') {
      steps {
        echo 'blah'
        checkout([$class: 'GitSCM', 
            branches: [[name: '${branch}']], 
            doGenerateSubmoduleConfigurations: false, 
            extensions: [], 
            submoduleCfg: [], 
            userRemoteConfigs: [[credentialsId: 'shywork', url: 'https://github.com/shayon83work/jenkinstest']]
        ])
        sh '''ls -l'''
      }
    }
  }
}
