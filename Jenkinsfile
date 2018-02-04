pipeline {
    agent any

    stages {

        stage ('Running AppScan') {
        node{
        appscan application: '36db3de9-7006-e811-9127-002590ac753d',
        credentials: 'Kripa\'s Asoc Account',
        name: 'test123',
        scanner: static-analyzer("C:/test_repositories/jenkins-example"),
        type: 'Static Analyzer'
        }

    }
}
}
