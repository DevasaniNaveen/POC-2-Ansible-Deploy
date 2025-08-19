pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package -f myapp/pom.xml'
      }
    }

    stage('Deploy') {
      steps {
        sh 'ansible-playbook -i "localhost," -c local deploy.yml'
      }
    }
  }
}
