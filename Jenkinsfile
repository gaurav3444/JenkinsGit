pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build the code using Maven'
            }
            post {
                always {
                   emailext  body: 'hi', subject: '', to: '3444gauravsharma@gmail.com'
              
            }
        }
       
        }

    }

}
