pipeline {
    agent any

    stages {
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