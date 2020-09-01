node{
    stage('SCM Checkout'){        
        git 'https://github.com/elisammg/FabricaDocker'
    }
    
    stage('Email Notification'){
        mail bcc: '', body: 'Jenkins', cc: '', from: '', replyTo: '', subject: 'Hello from Produccion', to: 'elisamargarita.2899@gmail.com'
    }
    
    stage('Compile-Package'){
        def mvnHome = tool name: 'maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    

    
   


}
