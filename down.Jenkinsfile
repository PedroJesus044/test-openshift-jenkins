pipeline {
    agent any

    stages {
        stage("Openshift Down") {
            steps {
                sh 'oc delete -f ./simple-nginx'
            }
        }
    }
}