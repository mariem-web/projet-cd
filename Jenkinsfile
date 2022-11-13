pipeline {
    agent any
    stages {
        stage ("Pull") {
            steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                    userRemoteConfigs:[[
                        credentialsId: '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', 
                           url: 'https://github.com/mariem-web/projet-cd.git']]])
                   }
                }
             }
      stage('Build'){
            steps{
                script{ 
                    sh "ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml -e ansible_become_password=123"
                }
            }
            }
         }
         
         }
