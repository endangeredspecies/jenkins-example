pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3.5' ,jdk:'ibm_jdk' ) {
                    bat 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0' ,jdk:'ibm_jdk') {
                    bat 'mvn test'
                }
            }
        }



    }
}
