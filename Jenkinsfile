@Library("Shared@main") _
pipeline{
    agent any
    
    stages{
        stage("Code Build"){
            steps{
                script{
                      dockerBuild("notes-app","latest")
                }
            
            }
        }

        stage("Docker image push")
        {
            steps{
                script{
                    dockerPush("dhalswapnil-dockerhub","notes-app","latest")
                }
            }
        }
        stage("Deploy"){
            steps{
                script{
                    dockerRun("notes-app","latest")
                }
            }
        }
    }
}
