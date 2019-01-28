node{

    stage('SCM Checkout'){

        git 'https://github.com/arjmsr/calcwebapp.git'

    }

    stage('Compile Package'){

        def mvnHome = tool name: 'MAVEN', type: 'maven'

        sh "${mvnHome}/bin/mvn package"

    }

    stage('Deploy to Tomcat'){ 

        sh 'cp target/*.war /usr/local/tomcat9/webapps'

    }

    stage('Email Notification'){

      mail bcc:'', body:'''Hi Welcome to Jenkins alerts

      Arjun Mishra''', cc:'', from:'', replyTo:'', subject:'Jenkins', to:'arjunmishra21dec@gmail.com'

    }

    

}
