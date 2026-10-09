pipeline {
agent any


stages {
    stage('Checkout') {
        steps {
            echo 'Pipeline started successfully.'
        }
    }

    stage('Build') {
        steps {
            echo 'Simulating application build.'
        }
    }

    stage('Test') {
        steps {
            echo 'Validating the Jenkinsfile.'
            sh 'test -f Jenkinsfile'
        }
    }
}

post {
    success {
        echo 'Pipeline completed successfully.'
    }

    failure {
        echo 'Pipeline failed. Check the console output.'
    }
}


}

