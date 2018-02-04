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
                withMaven(maven : 'maven_3.5' ,jdk:'ibm_jdk') {
                    bat 'mvn test'
                }
            }
        }

        stage ('Running AppScan') {

            steps {
                appscan application: '36db3de9-7006-e811-9127-002590ac753d',
                credentials: 'Kripa\'s Asoc Account',
                name: 'test123',
                scanner: 'static_analyzer("C:/test_repositories/jenkins-example")',
                type: 'Static Analyzer'
            }
        }




    }
}
