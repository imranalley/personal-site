//StartJenkinsFile!!!
pipeline {
    agent any
    stages {
        stage ('Deploy'){
            steps {
                script {
                    sh "ls"
                    sh """ssh $DeploymentUser@$DeploymentServer '
                    ls -la
                    '
                    """
                    sh "ls -la"
                    sh "exit"
                }
            }
        }
    }
}