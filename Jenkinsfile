pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -o cc_test ./main/cc_test.cpp'
            }
        }
        stage('Test'){
            steps{
                sh './cc_test'
                echo 'Test'
            }
        }
    }
    post{
        failure{
            echo 'failure happened'
        }
    }
}