pipeline {
    agent {label "maven"}
    stages {
        stage('Clone the repo') {
            steps {
                echo 'clone the repo'
                git branch: 'main',
				sh 'rm -fr html'
                sh 'git pull '
                
                
               
            }
        }
       
        stage('Check website is up') {
            steps {
                echo 'Check website is up'
                
            }
        }
    }
}