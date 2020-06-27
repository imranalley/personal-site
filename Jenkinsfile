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
                    cd personal-site
                    git status
                    git log
                    git fetch
                    git pull
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