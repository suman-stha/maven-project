pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                def mvnHome = tool name: 'mymaven', type: 'maven'
            def mvnCmd = "${mvnHome}/bin/mvn"
            sh "${mvnCmd} clean package"
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
