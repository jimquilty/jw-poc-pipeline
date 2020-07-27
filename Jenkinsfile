pipeline {
    agent any

    stages {
      stage('Download Kitchen File') {
          steps {
              git url: 'https://github.com/jimquilty/ansible-inspec.git'
          }
      }
      stage('Run Kitchen Destroy') {
        steps {
          bat 'kitchen destroy'
        }
      }
      stage('Run Kitchen Create') {
        steps {
          bat 'kitchen create'
        }
      }
      stage('Run Kitchen Converge') {
        steps {
          bat 'kitchen converge'
        }
      }
      stage('Run Kitchen Verify') {
        steps {
          bat 'kitchen verify'
        }
      }
      stage('Kitchen Destroy') {
        steps {
          bat 'kitchen destroy'
        }
      }
    }
}