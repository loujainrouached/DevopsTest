pipeline {
    agent any

   tools {
    maven 'MAVEN_HOME'
}


    options {
        timeout(time: 5, unit: 'MINUTES')
    }

    environment {
        APP_ENV = "DEV"
    }

    stages {

        

        stage('Code Build') {
            steps {
                sh 'mvn install -Dmaven.test.skip=true'
            }
        }
    }

    post {
        always {
            echo "======always======"
        }
        success {
            echo "=====pipeline executed successfully====="
        }
        failure {
            echo "======pipeline execution failed======"
        }
    }
}

