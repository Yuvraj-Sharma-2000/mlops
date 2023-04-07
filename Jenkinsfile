pipeline {
    agent any
    tools {
        // Manually specify the path to the Python executable
        // This assumes that Python is installed at C:\Python39\python.exe
        python '"C:\Users\Asus\AppData\Local\Programs\Python\Python310\python.exe"'
    }
    stages {
        stage('Git SCM Polling') {
            steps {
                git branch: 'main', url: 'https://github.com/Yuvraj-Sharma-2000/mlops.git'
            }
        }
        stage('Package') {
            steps {
                bat 'python setup.py sdist bdist_wheel'
            }
        }
        // stage('Provision Environment') {
        //     steps {
        //         ansiblePlaybook credentialsId: 'my-ansible-credentials', installation: 'my-ansible-installation', playbook: 'path/to/my/playbook.yml', inventory: 'path/to/my/inventory.ini'
        //     }
        // }
    }
}
