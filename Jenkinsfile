pipeline {
    agent any

    parameters {
        string(defaultValue: "3.9.3", description: 'pass the version of maven', name: 'maven_version')
    }

    stages {
       stage('download maven'){
         steps{
           sh 'cd/var/lib/jenkin'
           sh 'sudo wget https://dlcdn.apache.org/maven/maven-3/$maven_version/binaries/apache-maven-$maven_version-bin.tar.gz'
            
          }
       }
    }
  }
