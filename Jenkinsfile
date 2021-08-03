pipeline{
    agent{label 'master'}
    tools{maven 'M3'}
    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/Asharma-007/SpringPetClinic.git'
                
            }
        }
        stage('Build'){
            steps{
                sh 'mvn compile'
            }
        }
         stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('deploy'){
            steps{
                sh 'java -jar /var/lib/jenkins/workspace/PetClinnicDeclarativePipleline/target/*.jar'
            }
        }
    }
}
