pipeline {
    agent any
    
    parameters {
        string(name: 'INPUT_PARAM', defaultValue: 'default_value', description: 'Input parameter for Python script')
        string(name: 'INPUT_PARAM2', defaultValue2: 'default_value2', description: 'Input parameter for Python script2')
    }
    
    stages {
        stage('Invoke Python Script') {
            steps {
                script {
                    sh "python your_script.py '${params.INPUT_PARAM}' '${params.INPUT_PARAM2}'"
                }
            }
        }
    }
}
