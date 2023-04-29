pipeline {
    agent any
    stages {
        stage('build app') {
            steps {
               script {
                   echo "building the application..."
               }
            }
        }
        stage('build image') {
            steps {
                script {
                    echo "building the docker image..."
                }
            }
        }
        stage('deploy') {
            steps {
                script {
                   echo 'deploying docker image...'
                   withKubeConfig([credentialsId: 'lke-credentials', serverUrl: 'https://4bb845d7-22a1-474d-9dee-0718cfc32ab9.eu-central-2.linodelke.net']) {
                       sh 'kubectl create deployment nginx-deployment --image=nginx'
                   }
                }
            }
        }
    }
}