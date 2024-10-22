pipeline{
    agent any
    tools{maven 'M3'}
    stages{
        stage("checkout"){
            steps{
                git branch: 'main', url: 'https://github.com/Waseem-Ansari/SpringPetClinic.git'
            }
        }
        stage("Build"){
            steps{
                sh 'mvn compile'
            }
        }
        stage("Test"){
            steps{
                sh 'mvn test'
                
            }
        }
        stage("Package"){
            steps{
                sh 'mvn package'
            }
        }
        stage("Deploy"){
            steps{
                sh 'java -jar /home/coder/.jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar '
            }
            
        }
    }
}