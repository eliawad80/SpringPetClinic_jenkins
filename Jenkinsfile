pipeline{
    agent any
    stages{
        stage('Checkout'){
          steps{
               git branch: 'main' , url: 'https://github.com/eliawad80/SpringPetClinic_jenkins.git'
            }
        }

        stage('Test'){
            steps{
                sh 'mvn test'
                
            }
        }
        stage('Package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('Deploy'){
            steps{
                sh 'java -jar /var/lib/jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
            }
        
        }
        
    }
}

