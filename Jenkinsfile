pipeline {
    agent any
    
    parameters {
        string(name: 'INPUT_PARAM3', defaultValue: '', description: 'Input parameter for Python script')
        string(name: 'INPUT_PARAM4', defaultValue: '', description: 'Input parameter for Python script2')
    }
    
    stages {
        stage('Invoke Python Script') {
            steps {
                script {
                    sh "python hello.py '${params.INPUT_PARAM}' '${params.INPUT_PARAM2}'"
                }
            }
        }
    }
}
