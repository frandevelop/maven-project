pipeline{
    agent any
    
    tools{
        maven 'localMaven'
    }
    
    stages{
        stage('Build'){
            steps{
                bat 'mvn clean package'    
            }
            
            post{
                echo 'Estamos haciendo fuck archive de los arfecactos...'
                archiveArtifacts artifacts: '**/target/*.war'
            }
        }
    }
    
    stage('Deploy to staging'){
        steps{
            build jobs:'Deploy to fuck staging'
        }
    }
}
