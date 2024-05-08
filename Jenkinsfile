pipeline {

    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    // Checkout code from Git repository
                    checkout scm
                    checkout([$class: 'GitSCM', branches: [[name: '*/main']], 
                    doGenerateSubmoduleConfigurations: false, extensions: [], 
                    submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/mspavan77/test.git']]])

                    // Print list of files in the workspace
                    sh 'ls -la'
                }
            }
        }
        stage('Build') {
            agent { label 'pavan_label' }
                steps {
                echo "this is build stage"
                sh '''
                    cd /home/ubuntu/workspace/pipeline_1
                    make ABC.exe
                    exit 0
                    '''
        }
    }
        stage('Test') {
                steps {
                echo "this is a build test"
        }
    }
        stage('Deploy') {
                steps {
                echo "this is a build stage"
        }
    }
}
}
