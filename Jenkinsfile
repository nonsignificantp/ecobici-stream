pipeline {
  agent {
    docker {
      image 'tiangolo/uvicorn-gunicorn-fastapi'
      args '-p 80:80'
    }

  }
  stages {
    stage('server') {
      agent any
      steps {
        sh 'curl localhost'
      }
    }

  }
}