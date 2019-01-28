node{

    stage('Git Checkout'){

        git 'https://github.com/arjmsr/calcwebapp.git'

    }

    stage('Compile Test'){

        def mvnHome = tool name: 'MAVEN_HOME', type: 'maven'

        sh "${mvnHome}/bin/mvn package"

    }

    stage('Deploy'){ 

        sh 'cp target/*.war /usr/local/apache-tomcat9/webapps'

    }

    stage('Email Notification'){

      mail bcc:'', body:'''Hi Welcome to Jenkins alerts

      Arjun Mishra''', cc:'', from:'', replyTo:'', subject:'Jenkins', to:'arjunmishra21dec@gmail.com'

    }

    

}
