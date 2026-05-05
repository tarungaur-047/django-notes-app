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
                    docker_build("notes-app","latest",
        
