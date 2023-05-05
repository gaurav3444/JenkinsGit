pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build the code using Maven'
            }
            post {
                always {
                   mail attachLog: true, body: "Build successful", subject: "Build succeeded", to: '3444gauravsharma@gmail.com'
              
            }
        }
       
        }

    }

}
