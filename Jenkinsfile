pipeline {
    agent any
    tools { 
      maven 'MAVEN_HOME'
    }
    stages {
        stage('Polling') {
            steps {
                sh 'rm -rf taller-unistmo-spring-2023-2'
                sh 'git clone --branch feature_common_util_module https://github.com/JoseCaste/taller-unistmo-spring-2023-2.git'
            }
        }
        stage('Compilation'){
            steps{
                dir('taller-unistmo-spring-2023-2'){
                   sh 'mvn -o clean'
                   sh 'mvn -o install'
                }
            }
        }
    }
}
