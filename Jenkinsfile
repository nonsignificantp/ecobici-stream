pipeline {
  agent any
  stages {
    stage('server') {
      agent {
        docker {
          image 'tiangolo/uvicorn-gunicorn-fastapi'
          args '-p 80:80'
        }

      }
      steps {
        sh 'curl localhost'
      }
    }

  }
}