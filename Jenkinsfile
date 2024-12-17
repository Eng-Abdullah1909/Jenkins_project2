pipeline {
    agent any
    tools {
        maven "M399"
    }
    stages {
        stage(' Echo Version'){
            steps {
                sh 'echo Print Maven Version'
                sh 'mvn -version'
            }
        }
        stage ('build') {
            steps {
                sh "mvn clean package -DskipTests-true"
            }
       }
       stage ('unit test'){
            steps {
                sh "mvn test"
            }
        
       }
    }   
}
