pipeline {
    agent any
    tools {nodejs "mynodejs"}

    stages {
        stage('Dev') {
            steps {
                git 'https://github.com/harshal2112/JulyDemoRepo.git'
                echo "index.js file content "
            }
        }
        stage ('build') {
            steps {
               sh 'npm install'    
            }
        }
         stage ('withlogin') {
            steps {
            withCredentials([string(credentialsId: 'de69fc99-0319-4adc-bc6a-bd7b48cbc894', variable: 'myText')]) {
                 echo myText
              }   
            }
        }
    }
}