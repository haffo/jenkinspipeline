pipeline {
    agent any
    stages{
        // stage('Init'){
        //     steps {
        //         echo 'Testing...'
        //     }
        // }

        stage('Build'){
            steps {
                sh 'mvn clean install'
            }
            post {
                success {
                   echo 'Now archiving...'
                   archiveArtifacts artifacts '**/target/*.war'     
                }
            }
        }

        // stage('Deploy'){
        //     steps {
        //         echo 'Code deployed...'
        //     }
        // }

    }
}