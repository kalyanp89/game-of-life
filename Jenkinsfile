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
        stage('Build'){
            when {
                expression {
                    return "${GITS}" == "dev"
                }

               
            }
           
            steps {
                sh """
                
                  mvn clean package 
                  echo ${GITS}
                  echo teesting
                  echo I am from dev
                
                """
            }
        }
    }
}
