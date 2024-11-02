pipeline {
  agent {
    label 'nodejs'
  }

  stages {
    stage ('Install Dependencies') {
      steps {
        dir ('exchange-cli') {
          sh "npm install"
        }
      }
    }

    stage ('Build') {
      steps {
        dir ('exchange-cli') {
          sh "npm run build"
        }
      }
    }




  stage ('Unit Tests') {
    steps {
      dir ('exchange-cli') {
        sh "npm run test:unit"
      }
    }
  }
  stage ('Functional Tests') {
    steps {
      dir ('exchange-cli') {
        sh "npm run test:functional"
      }
    }
  }
  }
}
