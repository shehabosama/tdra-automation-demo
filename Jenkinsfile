pipeline {
    agent any

    stages {
     stage('Checkout') {
                steps {
                    // Checkout the code from the Git repository
                    git branch: 'master', url: 'https://github.com/shehabosama/tdra-automation-demo.git'
                }
            }
        stage('Trigger Child Pipeline Of Android Project') {
            steps {
                script {
                    def childPipeline = load 'jenkins_test_ci_cd/Jenkinsfile'
                    childPipeline.call()
                }
            }
        }
    }
}