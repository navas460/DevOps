pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        git(url: 'https://github.com/jenkins-docs/simple-node-js-react-npm-app.git', branch: 'master')
        sh '''#!/bin/bash

npm install'''
        nodejs 'NodeJS 15.13.0'
      }
    }

  }
}