pipeline {
  agent any
  parameters {
    string(name: 'branch', defaultValue: '', description: 'blah')
  }
  stages {
    stage('run') {
      steps {
        echo 'blah'
        //checkout([$class: 'GitSCM',
        //    branches: [[name: '${branch}']],
        //    userRemoteConfigs: [[credentialsId: 'shywork', url: 'https://github.com/shayon83work/jenkinstest']]
        //])
        git url: 'https://github.com/shayon83work/jenkinstest', branch: '${branch}', credentialsId: 'shywork'
        sh '''ls -l'''
      }
    }
  }
}
