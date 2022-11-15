pipeline {
    agent {label "maven"}
    
  //  environment {
//		DOCKERHUB_CREDENTIALS=credentials('	push-dockerhub')
//	}
    
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
          steps {
           
            sh 'docker build -t tpachat .'
    }
    
}
        
     //   stage('Login') {

//			steps {
//				 sh 'echo $dockerhubpwd'
  //               sh 'docker login -u $DOCKERHUB_CREDENTIALS_USR -p dckr_pat_MyHGGz-FUYMFBVVA-n8F44WUR2A'

	//		}
	//	}

	//	stage('Push') {

	//		steps {
	//		    sh 'docker tag tpachat ramzikhefifi/tpachat'
          //      sh 'docker push ramzikhefifi/tpachat'
				
		//	}
		//}
       
   
        
        
        
        
       
        
    }
}
