//StartJenkinsFile!!!
pipeline {
    agent any
    stages {
        stage ('Deploy'){
            steps {
                script {
                    withCredentials([sshUserPrivateKey(credentialsId: 'ssh-ubuntu-vpc', keyFileVariable: '', passphraseVariable: '', usernameVariable: '')]) {
                    sh "ls"
                    sh """ssh -tt $DeploymentUser@$DeploymentServer '
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
}