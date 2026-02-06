
pipeline{
    agent any

    environment{
        python='C:\\Users\\S\\AppData\\Local\\Programs\\Python\\Python313\\python.exe'
    }
    stages{
        stage('checkout code'){
            steps{
                checkout scm
            }
        }
        stage('setup python'){
            steps{
                bat '${env.python} extract.py'
            }
        }
    }

    post{
        success{
            echo 'pipeline completed'
        }
        failure{
            echo 'pipeline failed'
        }
        always{
            echo 'pipeline completed finished'
        }
    }
}