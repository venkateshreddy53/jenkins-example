pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                //withMaven(maven : 'maven_3_6') {
                    sh 'mvn clean compile'
   //             }
            }
        }

        stage ('Testing Stage') {

            steps {
              //  withMaven(maven : 'maven_3_6') {
                    sh 'mvn test'
   //             }
            }
        }


        stage ('Publish to Hygieia Stage') {
   
            steps {
                //withMaven(maven : 'maven_3_6') {
                    hygieiaBuildPublishStep buildStatus: 'Success'
  //              }
            }
        }
    }
}
