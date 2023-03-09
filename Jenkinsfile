pipeline{
    agent any
    stages{
        stage('sonar qulity status'){
            agent{
                docker{
                    image 'maven'
                }
            }

            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'snar-t') {
                    sh 'mvn clean package sonar:sonar'
    
                    }

                }
            }
        }
    }
}