pipeline {
    agent any

    environment {
        MY_NAME = 'deepu' // You can hardcode or make this a parameter
        MY_SECRET = credentials('my-secret-id') // This refers to a credential stored in Jenkins
    }

    stages {
        stage('Print Info') {
            steps {
                echo "Hello, my name is ${MY_NAME}"
                echo "print ${MY_SECRET}"
                // Do NOT print MY_SECRET directly - this is sensitive
                sh 'echo "My secret has been securely loaded."'
            }
        }
    }
}
