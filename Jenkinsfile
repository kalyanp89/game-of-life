pipeline {
    agent any
    environment {
        FULL_PATH_BRANCH = "${sh(script:'git name-rev --name-only HEAD', returnStdout: true)}"
        GITS = "${GIT_BRANCH.split("/")[1]}"
    }

    stages {
        stage('Git') {
            steps {
                git 'https://github.com/kalyanp89/game-of-life.git'
            
            }
        }    
        stage('Branch'){
            when {
                expression {
                    return "${GITS}" == "master"
                }

               
            }
        
            steps {
                sh "echo ${GITS}"
                sh "echo testing"
            }    
        
        }
    }
}

