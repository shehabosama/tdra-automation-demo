pipeline {
    agent any

     stages {
            stage('Stage 1') {
                steps {
                      git branch: 'master', url: 'https://github.com/shehabosama/tdra-automation-demo.git'
                }
            }

            stage('Stage 2') {
                steps {
                    // Your stage 2 steps here

                    script {
                        // Load and call child pipeline from a specific directory
                     //   def childPipeline = load 'path/to/childPipeline.groovy'
//                          def childPipeline = load 'jenkins_test_ci_cd/Jenkinsfile.groovy'
//
//                         childPipeline.call()
                           build job: 'pipeline_Android'
                    }
                }
            }
        }
}