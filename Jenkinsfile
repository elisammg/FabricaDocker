node{
    stage('SCM Checkout'){        
        git 'https://github.com/elisammg/FabricaDocker'
    }
    stage('Compile-Package'){
        def mvnHome = tool name: 'maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    
    stage('Sonarqube'){
        def mvnHome = tool name: 'maven', type: 'maven'
        withSonarQubeEnv('sonarqube'){
            sh "${mvnHome}/bin/mvn sonar:sonar"
        }
    }
    
   
    stage('Email Notification'){
        mail bcc: '', body: 'Jenkins', cc: '', from: '', replyTo: '', subject: 'Primera prueba', to: 'elisamargarita.2899@gmail.com'
    }

}
