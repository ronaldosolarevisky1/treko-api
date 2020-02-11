pipeline {
  agent {
    docker {
      image "node:8-alpine"
    }
  }
  stages {
    stage("Build") {
      steps {
        sh "chmod +x ./scripts/dropdb.sh"
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
