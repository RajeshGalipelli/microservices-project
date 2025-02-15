pipeline {
    agent any

    stages {
        stage("Build & Tag Docker Image") {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'docker-cred') {
                        sh 'docker build -t rajeshgalipelli089/frontend:v1 .'
            }
        }
    }
}
 stage("Push Docker Image"){
    steps{
        script {
            withDockerRegistry(credentialsId: 'docker-cred') {
                sh 'docker push rajeshgalipelli089/frontend:v1'
                }
            }
        }
    }
}
}
