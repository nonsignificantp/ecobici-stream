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
        sh '''touch myfile.txt
echo "hi there" >> myfile.txt'''
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

    stage('read with stash') {
      steps {
        unstash 'myfile'
        sh 'ls'
        sh 'cat myfile.txt'
      }
    }

  }
}