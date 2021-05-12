pipeline {
    agent any
    FULL_PATH_BRANCH = "${sh(script:'git name-rev --name-only HEAD', returnStdout: true)}"

    stages {
        stage('Git') {
            steps {
                git 'https://github.com/kalyanp89/game-of-life.git'
            
            }
        }    
        stage('Branch'){
        
            steps {
                sh "echo Branch: ${FULL_PATH_BRANCH}"
            }    
        
        }
    }
}

