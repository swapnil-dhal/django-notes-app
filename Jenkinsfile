pipeline{
    agent any
    
    stages{
        stage("Code Build"){
            steps{
            sh '''
            docker build -t notes-app .
            '''
            }
        }
        }
        stage("Deploy"){
            steps{
                sh '''
                docker run -d -p 8000:8000 notes-app:latest
                '''
            }
        }
        
    }
}
