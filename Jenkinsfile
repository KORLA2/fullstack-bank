pipeline{
    agent any
    environment{
        
        SONAR = tool 'sonarscanner'
    }

    stages{
    
stage('build and push'){
    steps{
        
   sh ' docker build -t backend .'
    }
}
        
    }
    post{
        always{
            echo "Iam always running"
        }
    }
}
