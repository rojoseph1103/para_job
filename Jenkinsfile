// Jenkins file (Declarative Pipeline)

pipeline {
   agent any
   parameters{
     string(name:'maven_version', defaultValue:'3.9.4', description:'pass the version of maven')
   }
  
    stages {
        stage('Download maven') {
            steps {
                sh 'cd /home'
                sh 'sudo wget https://dlcdn.apache.org/maven/maven-3/$maven_version/binaries/apache-maven-$maven_version-bin.tar.gz'
            }
        }
    }
  }
