pipeline {
    agent any

    stages {
        stage('Git') {
            steps {
                git 'https://github.com/kalyanp89/game-of-life.git'
            
            }
        }    
        stage('Branch'){
            when {
                expression {
                   env.GIT_BRANCH == "master"
                }
            }
        
            steps {
                sh "echo Branch: ${env.BRANCH_NAME}"
            }    
        
        }
    }
}

