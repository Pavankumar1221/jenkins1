pipeline {
    agent any

    environment {
        CUSTOM_VAR = "This is a custom environment variable"
    }

    stages {
        stage('Clone GitHub Repo') {
            steps {
                echo 'Code already checked out by Jenkins.'
            }
        }

        stage('Run Shell Script') {
            steps {
                sh 'chmod +x script.sh'
                sh './script.sh'
            }
        }

        stage('Print Working Directory Content') {
            steps {
                sh 'pwd'
                sh 'ls -la'
            }
        }

        stage('Use and Print Environment Variables') {
            steps {
                sh 'echo "Jenkins Home: $JENKINS_HOME"'
                sh 'echo "Custom Var: $CUSTOM_VAR"'
            }
        }
    }
}
