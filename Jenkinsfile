pipeline {
  agent any
  stages {
    stage('server') {
      agent {
        docker {
          image 'tiangolo/uvicorn-gunicorn-fastapi'
        }

      }
      steps {
        sh 'curl localhost'
      }
    }

  }
}