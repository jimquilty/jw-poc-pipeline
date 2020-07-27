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
          sh 'sudo kitchen destroy'
        }
      }
      stage('Run Kitchen Create') {
        steps {
          sh 'sudo kitchen create'
        }
      }
      stage('Run Kitchen Converge') {
        steps {
          sh 'sudo kitchen converge'
        }
      }
      stage('Run Kitchen Verify') {
        steps {
          sh 'sudo kitchen verify'
        }
      }
      stage('Kitchen Destroy') {
        steps {
          sh 'sudo kitchen destroy'
        }
      }
    }
}