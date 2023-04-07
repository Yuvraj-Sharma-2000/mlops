pipeline {
    agent any
    environment {
        PATH = "${env.PATH};"C:\\Python311\\"
    }
    stages {
        stage('Git SCM Polling') {
            steps {
                git branch: 'main', url: 'https://github.com/Yuvraj-Sharma-2000/mlops.git'
            }
        }
        stage('Install Python') {
            steps {
                bat 'choco install python3 -y'
            }
        }

        stage('Run Python Script') {
            steps {
                bat 'python3 myscript.py'
            }
        }
        // stage('Provision Environment') {
        //     steps {
        //         ansiblePlaybook credentialsId: 'my-ansible-credentials', installation: 'my-ansible-installation', playbook: 'path/to/my/playbook.yml', inventory: 'path/to/my/inventory.ini'
        //     }
        // }
    }
}
