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

        stage("Openshift remote execution 1") {
            steps {
                script {
                    openshift.withCluster( 'https://api.sandbox-m2.ll9k.p1.openshiftapps.com:6443', 'sha256~k9MWJl8gpbC3HqAh5L0J_boIRb66GBzt9eRnExjMYl0' ) {
                        openshift.withProject( 'pibarrap044-dev' ) {
                            echo "Hello from project ${openshift.project()} in cluster ${openshift.cluster()}"
                        }
                        }
                }
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