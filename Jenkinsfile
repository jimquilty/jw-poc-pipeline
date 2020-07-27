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
          pwsh 'kitchen destroy'
        }
      }
      stage('Run Kitchen Create') {
        steps {
          pwsh 'kitchen create'
        }
      }
      stage('Run Kitchen Converge') {
        steps {
          pwsh 'kitchen converge'
        }
      }
      stage('Run Kitchen Verify') {
        steps {
          pwsh 'kitchen verify'
        }
      }
      stage('Kitchen Destroy') {
        steps {
          pwsh 'kitchen destroy'
        }
      }
    }
}