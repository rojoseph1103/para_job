pipeline {
    agent any
    
    parameters {
        choice(name: 'MAVEN_VERSION', choices: ['3.8.4', '3.8.3', '3.8.2'], description: 'Select the Maven version to install')
    }
    
    stages {
        stage('Checkout') {
            steps {
                // You can add your repository checkout steps here if needed
                // For example, if you're using Git:
                // checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'your_git_repository_url']]])
            }
        }
        
        stage('Install Maven') {
            steps {
                script {
                    def mavenHome = tool name: 'Maven', type: 'hudson.tasks.Maven$MavenInstallation', installations: []
                    env.PATH = "${mavenHome}/bin:${env.PATH}"
                    sh "echo 'export PATH=${mavenHome}/bin:\$PATH' >> ~/.bashrc"
                }
            }
        }
        
        stage('Build') {
            steps {
                // Add your Maven build commands here
                // For example, "mvn clean install"
                sh "mvn clean install"
            }
        }
    }
    
    post {
        success {
            // You can add post-build steps here, e.g., notifications or deployment
        }
    }
}
