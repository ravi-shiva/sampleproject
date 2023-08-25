pipeline {
  agent any
  stages {
    stage('fetch code') {
      steps {
        git(url: 'https://github.com/ravi-shiva/sampleproject.git', branch: 'main')
      }
    }

    stage('Install Apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('deploy app') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}