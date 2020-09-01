node{
    stage('SCM Checkout'){
        git 'https://github.com/elisammg/FabricaDocker'
    }
    stage('Compile-Package'){
        sh 'mvn package'
    }
    
    stage('Email Notification'){
        mail bcc: '', body: 'Jenkins', cc: '', from: '', replyTo: '', subject: 'Jenkins', to: 'elisamargarita.2899@gmail.com'
    }

}
