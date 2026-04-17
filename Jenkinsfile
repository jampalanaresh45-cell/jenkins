pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        COURSE = "DevOps"   // Define any environment variables here if needed
    }

    stages { 
        stage('Build') {
            steps {
                script {
                    sh """
                        echo "Building"
                        echo $COURSE
                    """
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh """
                        echo "Testing"
                    """
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    sh """
                        echo "Deploying"
                    """
                }
            }
        }
    }

    post {
        always { 
            echo "I'll always say Hello World!"
            cleanWs()
        }
        success {
            echo "This will run only if the build succeeds."
        }
        failure {
            echo "This will run only if the build fails."
        }
    }
}