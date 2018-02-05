pipeline {
    agent any

    appscan application: '36db3de9-7006-e811-9127-002590ac753d', credentials: 'cred', name: 'test12345', scanner: $static-analyzer('C:/work/src'), type: 'Static Analyzer'
}
