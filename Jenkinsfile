pipeline {

  agent any
  parameters {
        string(name: 'maven_version', defaultValue: '3.8.8', description: 'pass the version of maven')
  }
	
    stages {
        stage('download maven') {
            steps {
                sh 'cd /var/lib/jenkins/'
                sh 'sudo wget 'https://dlcdn.apache.org/maven/maven-3/3.8.8/binaries/apache-maven-3.8.8-bin.tar.gz'
            }
        }
    }
}
