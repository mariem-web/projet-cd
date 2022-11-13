pipeline {
    agent any
    stages {
        stage ("Pull") {
            steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                    userRemoteConfigs:[[
                        credentialsId: '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', 
                           url: 'https://github.com/mariem-web/cdd.git']]])
                   }
                }
             }
         }
         
         }
