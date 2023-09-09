pipeline {
    agent any

    parameters {
        string(defaultValue: "3.9.3", description: 'pass the version of maven', name: 'maven_version')
    }

    stages {
        stage('download maven'){
            steps{
                sh 'cd /var/lib/jenkins/'
				sh 'https://dlcdn.apache.org/maven/maven-3/3.8.8/binaries/apache-maven-3.8.8-bin.tar.gz'
            }
        }
    }
}
