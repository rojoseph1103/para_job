pipeline {
    agent any
    parameters {
        string(name: 'maven_version', defaultValue: '3.9.3', description: 'pass the version of maven')
    }
    stages {
        stage('download maven') {
            steps {
		sh 'cd /var/lib/jenkins/'    
                sh 'sudo wget https://apache.mirror.digitalpacific.com.au/maven/maven-3/${params.maven_version}/binaries/apache-maven-${params.maven_version}-bin.tar.gz'

            }
        }
   }
}
