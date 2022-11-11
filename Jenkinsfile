pipeline {
    agent {label "maven"}
    stages {
        stage('Clone the repo') {
            steps {
                echo 'clone the repo'
                sh 'rm -fr html'
                sh   'rm -rf projetDevops'
                sh 'git clone https://github.com/RamziKhefifi/projetDevops.git'
                
                
               
            }
        }
       
        stage('Check website is up') {
            steps {
                echo 'Check website is up'
                
            }
        }
    }
}
