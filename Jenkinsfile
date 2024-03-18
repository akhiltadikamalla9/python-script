pipeline {
    agent any
    
    parameters {
        string(name: 'INPUT_PARAM', defaultValue: '', description: 'Input parameter for Python script')
        string(name: 'INPUT_PARAM2', defaultValue: '', description: 'Input parameter for Python script2')
    }
    
    stages {
        stage('Invoke Python Script') {
            steps {
                script {
                    bat "python hellow.py '${params.INPUT_PARAM}' '${params.INPUT_PARAM2}'"
                }
            }
        }
    }
}
