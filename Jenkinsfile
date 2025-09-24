pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'docker build -t sudhamaibathula/adservice:v1'
            }
        }
        stage("Push"){
            steps{
                script{
                    withDockerRegistry(credentialsId: 'admin') {
                        sh 'docker push sudhamaibathula/adservice:v1'
                    }
                }
                
            }
        }
    }
}
