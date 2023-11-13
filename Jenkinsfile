pipeline{
    agent any
  tools{
      dockerTool 'Docker'
  }
    
    stages{
    
stage('build and push'){
    steps{
        
   sh ' docker -v'
    }
}
        
    }
    post{
        always{
            echo "Iam always running"
        }
        success{
              echo "Iam  running in success"
        }
        failure{
             echo "Iam  running in failure"
        }
    }
}
