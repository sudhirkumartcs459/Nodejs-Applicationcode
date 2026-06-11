pipeline {

    agent any

    stages {

        stage('Docker Login Test') {
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: 'dockerhub-creds',
                        usernameVariable: 'DOCKER_USER',
                        passwordVariable: 'DOCKER_PASS'
                    )
                ]) {
                    bat '''
                    docker logout
                    docker login -u "%DOCKER_USER%" -p "%DOCKER_PASS%"
                    '''
                }
            }
        }
    }
}
