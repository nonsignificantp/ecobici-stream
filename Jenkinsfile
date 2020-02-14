pipeline {
  agent any
  stages {
    stage('create file') {
      agent {
        docker {
          image 'python:3.7-slim'
          args '-u root'
        }

      }
      steps {
        sh '''echo "create file"










&& touch myfile.txt'''
        stash(name: 'myfile', includes: '**/*.txt')
      }
    }

    stage('read directory') {
      agent {
        docker {
          image 'python:3.7-slim'
        }

      }
      steps {
        sh 'ls'
      }
    }

  }
}