@Library ("shared") _
pipeline{

    agent { label "James"}

    stages{

        stage("hello"){
            steps{
                script{
                    hello()
                }
            }

        }
        stage("Code"){
            steps{
                script{
                    clone("https://github.com/tarungaur-047/django-notes-app.git","main")
                }
            }
        }
        stage("Build"){
            steps{
                script{
                 //pulling image direct from dockerhub
                    build("notes-app","latest","tarungaur")
                }
            }
        }
        stage("Push to DockerHub"){
            steps{
                script{
                    dockerpush("notes-app","latest","tarungaur")
                }
            }
        }
        stage ("Deploy"){
            steps{
                echo " the code is being deployed " 
                sh " docker compose up -d " 
            }
        }
    }
}
        
