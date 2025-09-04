pipeline{
    agent any
    
    stages{
        stage("Code Build"){
            steps{
            dockerbuild("notes-app","latest")
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
