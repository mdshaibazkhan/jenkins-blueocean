pipeline {
  agent any
  stages {
    stage('Fetch code') {
      steps {
        git(url: 'https://github.com/mdshaibazkhan/jenkins-blueocean.git', branch: 'main', poll: true)
      }
    }

    stage('Install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Deploy code') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}