pipeline {
    agent any
    
    parameters {
        string(name: 'MAVEN_VERSION', defaultValue: '3.9.3', description: 'Enter the Maven version to install (e.g., 3.8.4)')
    }
    
    stages {
        stage('download maven') {
            steps {
	       sh 'cd /var/lib/jenkins/'    
               sh 'sudo wget https://dlcdn.apache.org/maven/maven-3//$maven_version/binaries/apache-maven-$maven_version-bin.tar.gz'
            }
          
        }
    }
}

