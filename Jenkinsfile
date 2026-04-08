pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/2025sl93018-cmd/labsheet1-93018.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build Stage'
            }
        }

        stage('Test') {
            steps {
                sh '''
                python3 - <<EOF
import calculator
assert calculator.add(2,3) == 5
assert calculator.subtract(5,3)==2
assert calculator.divide(6,3)==2
assert calculator.multiply(2,3) == 6
print("All tests passed")
EOF
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy Stage'
            }
        }
    }
}
