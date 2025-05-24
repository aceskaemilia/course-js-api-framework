pipeline {
    agent any
    stages {
        stage('build-api-test-image') {
            steps {
                builDockerImage()
            }
        }
    }
}

def builDockerImage(){
    echo "Building of node application is starting.."
    sh "docker build -t aceskaemilija/api-tests ."

    echo "Pushing image to docker registry.."
    sh "docker push aceskaemilija/api-tests"
}