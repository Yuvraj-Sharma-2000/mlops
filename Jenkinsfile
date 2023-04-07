pipeline {
    agent any
    stages {
        stage('Git SCM Polling') {
            steps {
                git branch: 'main', url: 'https://github.com/Yuvraj-Sharma-2000/mlops.git'
            }
        }
        stage('Install Python') {
            steps {
                bat 'start /B python myscript.py'
            }
        }
        stage('Package') {
            steps {
                bat 'python3 setup.py sdist bdist_wheel'
            }
        }
        // stage('Provision Environment') {
        //     steps {
        //         ansiblePlaybook credentialsId: 'my-ansible-credentials', installation: 'my-ansible-installation', playbook: 'path/to/my/playbook.yml', inventory: 'path/to/my/inventory.ini'
        //     }
        // }
    }
}
