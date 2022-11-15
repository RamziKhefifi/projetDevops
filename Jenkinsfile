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
        
        stage('MNV CLEAN') 
        
        { steps 
         { 
         sh 'mvn clean' 
         
         } 
        }
       
        stage ('Maven Compile') {
            steps {

                sh "mvn compile"
            }
        }
        stage('Build the artifact'){
            steps{
                sh "mvn package"
            }
            }
        
        stage('BUILDING IMAGE'){
          steps 
            sh 'docker build -t tpachat .'
    }
    
      
       
   
        
        
        
        
       
        
    }
}
