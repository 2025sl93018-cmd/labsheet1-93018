pipeline {

    agent any
 
    stages {

        stage('Checkout') {

            steps {

                git branch: 'main', url: 'https://github.com/2025sl93018-cmd/labsheet1-93018.git'

            }

        }
 
        stage('Build') {

            steps {

                sh 'echo Build stage'

            }

        }
 
        stage('Test') {

            steps {

                sh '''

                python3 -c "

import calculator

assert calculator.add(2,3)==5

assert calculator.multiply(2,3)==6

assert calculator.subtract(5,3)==2

assert calculator.divide(6,2)==3

"

                '''

            }

        }
 
        stage('Deploy') {

            steps {

                sh 'echo Deploy stage'

            }

        }

    }

}
 
