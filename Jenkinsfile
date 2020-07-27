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
          powershell 'kitchen destroy'
        }
      }
      stage('Run Kitchen Create') {
        steps {
          powershell 'kitchen create'
        }
      }
      stage('Run Kitchen Converge') {
        steps {
          powershell 'kitchen converge'
        }
      }
      stage('Run Kitchen Verify') {
        steps {
          powershell 'kitchen verify'
        }
      }
      stage('Kitchen Destroy') {
        steps {
          powershell 'kitchen destroy'
        }
      }
    }
}