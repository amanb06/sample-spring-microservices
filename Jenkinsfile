pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
       /* stage('Validation') {
        steps {
        //Moving in to the directory to execute the commands
        dir('account-service') {
            script {
                //Using the git command to check the difference between previous successful commit. ${GIT_PREVIOUS_SUCCESSFUL_COMMIT} is an environment variable comes with GIT Jenkins plugin
                //There is a drawback though, if it is the first time you are running this job, this variable is not available and fails the build
                //For the first time i had to use ${env.GIT_COMMIT} itself at both places to pass the build. A hack but worth it for future builds.

                def strCount = sh(returnStdout: true, script: "git diff --name-only ${env.GIT_COMMIT} ${GIT_PREVIOUS_SUCCESSFUL_COMMIT} | grep account-service | wc -l").trim()
                if(strCount=="0") {
                    echo "Skipping build no files updated"
                    CONTINUE_BUILD = false
                } else {
                    echo "Changes found in the account-service module"
                }
            }
        }
       dir('customer-service') {
            script {
                //Using the git command to check the difference between previous successful commit. ${GIT_PREVIOUS_SUCCESSFUL_COMMIT} is an environment variable comes with GIT Jenkins plugin
                //There is a drawback though, if it is the first time you are running this job, this variable is not available and fails the build
                //For the first time i had to use ${env.GIT_COMMIT} itself at both places to pass the build. A hack but worth it for future builds.

                def strCount = sh(returnStdout: true, script: "git diff --name-only ${env.GIT_COMMIT} ${GIT_PREVIOUS_SUCCESSFUL_COMMIT} | grep customer-service | wc -l").trim()
                if(strCount=="0") {
                    echo "Skipping build no files updated"
                    CONTINUE_BUILD = false
                } else {
                    echo "Changes found in the customer-service module"
                }
            }              
    } 
}
        } */
    }
}
