node{
    stage('SCM Checkout'){
        git 'https://github.com/elisammg/FabricaDocker'
    }
    stage('Compile-Package'){
        def mvnHome = tool name: 'maven-3', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Email Notification'){
        mail bcc: '', body: 'Jenkins', cc: '', from: '', replyTo: '', subject: 'Jenkins', to: 'elisamargarita.2899@gmail.com'
    }

}
