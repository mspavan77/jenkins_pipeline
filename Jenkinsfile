pipeline {

agent any
stages {
    stage('Build') {
        agent { label 'pavan_label' }
        steps {
            echo "Success"
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
