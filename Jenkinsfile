node{

    stage('SCM Checkout'){

        git ''

    }

    stage('Compile Package'){

        def mvnHome = tool name: 'MAVEN', type: 'maven'

        sh "${mvnHome}/bin/mvn package"

    }

    stage('Deploy to Tomcat'){ 

        sh 'cp target/*.war /usr/local/tomcat9/webapps'

    }

    stage('Email Notification'){

      mail bcc:'', body:'''Hi Welcome to Jenkins Pipeline alerts

      Thanks

      M.Muniraja''', cc:'', from:'', replyTo:'', subject:'Jenkins Job', to:'mmuni1990@gmail.com'

    }

    

}
