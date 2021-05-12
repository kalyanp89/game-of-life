pipeline {
    agent any
    environment {
        FULL_PATH_BRANCH = "${sh(script:'git name-rev --name-only HEAD |awk -F "/" '{print $2}' ', returnStdout: true)}"
        GITS = "${GIT_BRANCH}"
    }

    stages {
        stage('Git') {
            steps {
                git 'https://github.com/kalyanp89/game-of-life.git'
            
            }
        }    
        stage('Branch'){
        
            steps {
                sh "echo ${GITS}"
            }    
        
        }
    }
}

