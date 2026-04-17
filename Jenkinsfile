pipeline {
    agent{
        node {
            label 'AGENT-1'
        }
    
    }
    stages 
        stage('Build') {
            steps {
                script{
                    sh """
                        echo "Building"
                    """
                }
            }
        }
        stage('Test') {
            steps {
                script{
                    sh """
                        echo "Building"
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script{
                    sh """
                        echo "Building"
                }    """
            }
        }
    }
    post{
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