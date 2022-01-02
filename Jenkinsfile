pipeline {
    agent any

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
}
