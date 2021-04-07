pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        git(url: 'https://github.com/jenkins-docs/simple-node-js-react-npm-app.git', branch: 'master')
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        sh 'test.sh'
      }
    }

    stage('Deliver') {
      steps {
        sh 'deliver.sh'
        input 'Finished using the web site? (Click "Proceed" to continue)'
        sh 'kill.sh'
      }
    }

  }
  tools {
    nodejs 'node'
  }
}
