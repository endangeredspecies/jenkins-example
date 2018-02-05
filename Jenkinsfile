
pipeline {
    agent any

    stages {
        stage ('build') {
        appscan application: '36db3de9-7006-e811-9127-002590ac753d', credentials: 'cred', name: 'test_random3', scanner: 'static-analyzer',target:'C:/work/src', type: 'Static Analyzer' 

        }

    }
}
