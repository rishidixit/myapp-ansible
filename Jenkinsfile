pipeline{
    agent any
    stages{
        stage("GIT Checkout") {
            steps {
                git credentialsId: 'github', url: 'https://github.com/rishidixit/myapp-ansible'
            }
        }
        stage("Ansible Deployment") {
            steps {
                ansiblePlaybook credentialsId: 'Apache-Node', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dev.inv', playbook: 'apache.yml'
            }
        }
    }
}
