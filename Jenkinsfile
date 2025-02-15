pipeline {
    agent any

    stages {
        stage("Build & Tag Docker Image") {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'docker-cred') {
                        sh 'docker build -t rajeshgalipelli089/currencyservice:v1 .'
            }
        }
    }
}
 stage("Push Docker Image"){
    steps{
        script {
            withDockerRegistry(credentialsId: 'docker-cred') {
                sh 'docker push rajeshgalipelli089/currencyservice:v1'
                }
            }
        }
    }
}
}

