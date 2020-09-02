node{
    stage('SCM Checkout'){        
        git 'https://github.com/elisammg/FabricaDocker'
    }
    
    stage('Email Notification'){
        mail bcc: '', body: 'Jenkins', cc: '', from: '', replyTo: '', subject: 'Hello from Dev', to: 'jflores@unis.edu.gt'
    }
    
    stage('Compile-Package'){
        def mvnHome = tool name: 'maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    

    
   


}
