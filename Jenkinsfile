pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/sraj9506/Day13.git', branch: env.BRANCH_NAME
            }
        }

        stage('Build') {
            steps {
                script {
                    echo "Building from ${env.BRANCH_NAME} branch : "
                    sh 'javac Sample.java'
                    sh 'java Sample'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo "Running Deployment from ${env.BRANCH_NAME} branch :"
                    sh 'javac Sample.java'
                    sh 'java Sample'
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished.'
        }
        success {
            echo 'Pipeline succeeded.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
