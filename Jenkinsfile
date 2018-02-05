
pipeline {
    agent any

    stages {
        stage ('Running AppScan') {
        steps{
          application: '36db3de9-7006-e811-9127-002590ac753d', credentials: 'cred', name: 'test12345', target: 'C:/work/src', type: 'Static Analyzer'
        }


        }

    }
}
