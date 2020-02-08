pipeline {
    agent { docker 'python:3.6.5' }
    stages {
        stage('build') {
            steps {
                sh 'python --version >> py.version'
            }
        }
        stage('test') {
            steps {
                sh 'ps aux >> ps.res'
            }
        }

    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
