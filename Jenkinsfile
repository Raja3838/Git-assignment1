pipeline {
    agent any
    stages {
        stage('Input') {
            steps {
                script {
                    def releaseNames = ['ssd-api', 'ssd-lops-api']
                    def releaseName = input(
                        id: 'ReleaseName',
                        message: 'Select release name',
                        parameters: [
                            choice(name: 'ReleaseName', choices: releaseNames, description: 'Choose the name')
                        ]
                    )
                    echo "Selected release name: $releaseName"
                }
            }
        }
        stage('Your Custom Stage 1') {
            steps {
                script {
                    echo "This is my name: $releaseName"
                    // Assuming you'll be doing something more meaningful with the releaseName in this stage.
                }
            }
        }
    }
}

// This is just a placeholder function. Implement your own logic to fetch the last version.
def getLastVersion(serviceName) {
    // Replace this with your command or API call to get the last version for the service.
    return "last-version-for-$serviceName"
}
