pipeline {
    agent {label "maven"}
    stages {
          stage ('Git') {
            steps {
                echo 'pulling...';
                git branch :'main' ,
           
                url : 'https://github.com/RamziKhefifi/projetDevops.git'
            }
        }
       
       
        stage('Check website is up') {
            steps {
                echo 'Check website is up'
                
            }
        }
    }
}
