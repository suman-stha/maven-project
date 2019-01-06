node{
    stage('SCM Checkout'){
        git 'https://github.com/suman-stha/maven-project.git'

    }
    stage('Compile and Build'){
        def mvnHome = tool name: 'mymaven', type: 'maven'
		sh "${mvnHome}/bin/mvn package"
    }
    stage('Build Docker Image'){
        sh 'docker build -t sumand123/maven-project:1.0.0 .'
    }
}
