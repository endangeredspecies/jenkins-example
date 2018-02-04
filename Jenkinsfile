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
                appscan (application: '36db3de9-7006-e811-9127-002590ac753d', credentials: 'Kripa\'s Asoc Account', email: true, name: 'test_pipe_line_static_analysis_04022018', scanner: appscan('C:\\\\test_repositories\\\\jenkins-example'), type: 'Static Analyzer')
            }
        }




    }
}
