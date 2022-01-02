pipeline {
    agent any
    parameters {
            choice(name: 'environment', choices: ['dev', 'uat', 'prod'], description: 'Select environment to deploy')
        }
    stages {
      stage('User input') {
            input {
                message "Give some string"
                ok "Test input"
                parameters {
                    string(name: 'testString', defaultValue: 'None', description: 'Test string input')
                }
            }
            steps {
                echo "Your string ${testString}"
            }
        }
    }
    post {
                    always {
                        echo 'Job ends'
                    }
                    success {
                        echo 'Job is success'
                    }
                    failure {
                        echo 'Job is failure'
                    }
                }
}
