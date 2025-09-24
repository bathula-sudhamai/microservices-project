pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'docker build -t sudhamaibathula/currencyservice:v1'
            }
        }
        stage("Push"){
            steps{
                script{
                    withDockerRegistry(credentialsId: 'admin') {
                        sh 'docker push sudhamaibathula/currencyservice:v1'
                    }
                }
                
            }
        }
    }
}
