pipeline {

    agent any
    stages {
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
