pipeline {

    agent any

    stages {

        stage('Check Docker Credentials') {
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: 'dockerhub-creds',
                        usernameVariable: 'DOCKER_USER',
                        passwordVariable: 'DOCKER_PASS'
                    )
                ]) {
                    bat '''
                    echo Docker Username: %DOCKER_USER%
                    '''
                }
            }
        }
    }
}
