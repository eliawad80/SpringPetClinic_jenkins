pipeline{
    agent any
    tools{ mvnw }
    stages{
        stage('Checkout'){
          steps{
               git branch: 'main' , url: 'https://github.com/eliawad80/SpringPetClinic_jenkins.git'
            }
        }
        stage('Compile'){
            steps{
                sh './mvnw compile'
            }
        }
        stage('Test'){
            steps{
                sh './mvnw test'
                
            }
        }
        stage('Package'){
            steps{
                sh './mvnw package'
            }
        }
        stage('Deploy'){
            steps{
                sh 'java -jar /var/lib/jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
            }
        
        }
        
    }
}

