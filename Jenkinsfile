pipeline {

    agent any 

    stages {

        stage('checkout') { 

            steps {

                git url:'https://github.com/jyotheesh/library-new-FC.git'

            }

        }

        
          stage('Build') { 

            steps {

                sh '''
              npm install
              ng build --base-href="./"
            '''

            }

        }
  stage('Deploy') { 

            steps {

                sh '''
                cd /var/lib/jenkins/workspace/ffff/dist
                chmod -R 777 AngularProject
                cp -rf AngularProject /opt/apache-tomcat-9.0.26/webapps/
            '''

            }

        }

    }

}
