pipeline {
    agent any
    
    parameters {
        string(name: 'dev_workspace_id', defaultValue: '', description: 'Input parameter for Python script')
        string(name: 'test_workspace_id', defaultValue: '', description: 'Input parameter for Python script2')
    }
    
    stages {
        stage('Invoke Python Script') {
            steps {
                script {
                    bat "python hellow.py '${params.dev_workspace_id}' '${params.test_workspace_id}'"
                }
            }
        }
    }
}
