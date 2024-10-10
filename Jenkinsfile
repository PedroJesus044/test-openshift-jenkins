pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage("Checkout") {
            steps {
                checkout scm
            }
        }

        // stage("Openshift Apply") {
        //     steps {
        //         sh 'oc apply -f ./simple-nginx'
        //     }
        // }

        // stage("Openshift Build") {
        //     steps {
        //         sh 'oc start-build hello-openshift'
        //     }
        // }
    }
}