pipeline {
    agent {label "maven"}
    stages {
          stage ('Git') {
            steps {
                echo 'pulling...';
                git branch :'main' ,
           
                url : 'https://github.com/RamziKhefifi/projetDevops.git'
                //credentialsId: 'accgithubjenkins';
            }
        }
       
       
        stage('Check website is up') {
            steps {
                echo 'Check website is up'
                
            }           
        }
        
        
        stage('MNV CLEAN') {
            steps {
                sh 'mvn clean'
            }
        }
       stage('MVN COMPILE') {
            steps {
                sh 'mvn compile'
            }
        }
        
        
    }
}
