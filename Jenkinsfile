pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'docker build -t sudhamaibathula/productcatalogservice:v1 .'
            }
        }
        stage("Push"){
            steps{
                script{
                    withDockerRegistry(credentialsId: 'admin') {
                        sh 'docker push sudhamaibathula/productcatalogservice:v1'
                    }
                }
                
            }
        }
    }
}
