pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build the code using Maven'
            }
            post {
                always {
                   emailext attachLog: true, body: '', subject: '', to: '3444gauravsharma@gmail.com'
              
            }
        }
       
        }

    }

}
