<<<<<<< HEAD
pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'mvn clean package'
=======

pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                
		sh 'mvn clean package'
                
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
>>>>>>> a14a94a94b4865692bd94cf934ae33a58e8b534a
            }
        }
    }
}
