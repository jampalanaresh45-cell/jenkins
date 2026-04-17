pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        COURSE = "DevOps"   // Define any environment variables here if needed
    }
    options {
        timeout(time: 10, unit: 'SECONDS')   // Add any pipeline options here if needed
    }
    stages { 
        stage('Build') {
            steps {
                script {
                    sh """
                        echo "Building"
                        echo $COURSE
                        sleep 10
                        env
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
        aborted {
            echo "Pipeline is aborted."
        }
    }
}