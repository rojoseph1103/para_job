pipeline {
    agent any
    parameters {
        string(name: 'maven_version', defaultValue: '3.9.3', description: 'pass the version of maven')
    }
    stages {
        stage('download maven') {
            steps {
                script {
                    sh "cd /var/lib/jenkins/"
                    sh "sudo wget https://dlcdn.apache.org/maven/maven-3/${params.maven_version}/binaries/apache-maven-${params.maven_version}-bin.tar.gz"
                }
            }
        }
    }
}
