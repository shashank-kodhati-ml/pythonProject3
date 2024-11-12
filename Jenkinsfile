pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout([
                        $class: 'GitSCM',
                        branches: [[name: '*/main']],  // or any branch you want to checkout
                        userRemoteConfigs: [[
                            url: 'https://github.com/your-username/your-repository.git',
                            credentialsId: 'your-credential-id'  // The credential ID you set in Jenkins
                        ]]
                    ])
                }
            }
        }
        stage('Build') {
            steps {
                echo 'Building project...'
            }
        }
    }
}
