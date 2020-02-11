pipeline {
  agent {
    docker {
      image "node:8-alpine"
    }
  }
  stages {
    stage("Build") {
      steps {
        sh "npm install"
      }
    }
    stage("test") {
      steps {
        sh "npm run test:ci"
      }
    }
  }
}
