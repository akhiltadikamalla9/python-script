pipeline {
    agent any
    
    parameters {
        string(name: 'dev_workspace_id', defaultValue: '2a69087b-8a81-499c-b3c4-ac69d5795d00,eef6b44c-572a-4776-b050-ef089f968e73', description: 'Input parameter for Python script')
        string(name: 'test_workspace_id', defaultValue: 'ca199a86-1305-462f-8ae5-e4fc8f5268d7,86a33025-b2f0-49d7-b383-0c3fe25ea808', description: 'Input parameter for Python script2')
    }
    
    stages {
        stage('Parse Parameters') {
            steps {
                script {
                    // Initialize ArrayLists to store parsed parameters
                    def param1List = []
                    def param2List = []
                    
                    // Check if parameters are provided and not empty
                    if (params.dev_workspace_id && params.test_workspace_id) {
                        // Split parameters into lists
                        param1List = params.dev_workspace_id.split(',')
                        param2List = params.test_workspace_id.split(',')
                    } else {
                        error "Parameters are not provided or empty"
                    }
                    
                    // Call Python script and pass ArrayLists as command-line arguments
                    def result = sh(script: "python hellow.py '${param1List.join(',')}' '${param2List.join(',')}'", returnStdout: true).trim()
                    echo "Result from Python script: ${result}"
                }
            }
        }
    }
}
