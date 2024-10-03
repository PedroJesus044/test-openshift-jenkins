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
        stage("Openshift Apply") {
            steps {
                sh 'oc apply -f ./simple-nginx'
            }
        }
        stage("Openshift Build") {
            steps {
                sh 'oc start-build hello-openshift'
            //   sh '''
            //       #oc start-build --from-build=<build_name>
            //       #oc start-build -F red-api --from-dir=./api/
            //       oc start-build hello-openshift
                  
            //   '''
            }
        }
    }
}