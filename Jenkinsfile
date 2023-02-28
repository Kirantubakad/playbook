pipeline{
    agent any
    stages{
        stage('scm checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/Kirantubakad/playbook.git'
            }
        }
        
        stage('ansible-playbook'){
            steps{
                ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'ansible', inventory: 'inventory', playbook: 'apache.yaml'
            }
        }
    }
}
