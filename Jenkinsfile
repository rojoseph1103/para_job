pipeline {

  agent any
  parameters {
        string(name: 'maven_version', defaultValue: '3.9.4', description: 'pass the version of maven')
  }
	
    stages {
        stage('download maven') {
            steps {
                sh 'cd /var/lib/jenkins/'
                sh 'sudo su - https://dlcdn.apache.org/maven/maven-3/$maven_version/binaries/apache-$maven_version-bin.tar.gz'
            }
        }
	

    }
}
