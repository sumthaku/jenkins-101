pipeline {
    agent any  // Corrected syntax for agent block
    triggers {
        pollSCM('* * * * *') // Ensure to format cron expression properly
    }
    stages {
        stage('Build') {
            steps {
                echo "Build.."
                sh '''
                cd myapp
                pip install -r requirements.txt
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                cd myapp
                python3 hello.py
                python3 hello.py --name=Brad
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
