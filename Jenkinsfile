def mvnHome = tool name: 'mymaven', type: 'maven'
pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                
		sh "${mvnHome}/bin/mvn package"
                
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
