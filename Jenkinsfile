pipeline {

  agent any
  parameters {
        string(name: 'maven_version', defaultValue: '3.9.3', description: 'pass the version of maven')
  }
	
    stages {
        stage('download maven') {
            steps {
                sh 'cd/opt /var/lib/jenkins/'
                sh 'sudo wget https://dlcdn.apache.org/maven/maven-3/$maven --version/binaries/apache-$maven --version-bin.tar.gz'
            }
        }
    }
}
