pipeline {
parameters {
 string (name : 'version', description: 'the newest version' )
choices (name:'mychoice' , choices:['1.0','1.1','1.2'] )

 }
 agent any
  stages {
    stage('parameters') {
      steps  {
      echo "Iam ${params.version} ${params.mychoice}" // Now I can use docker commands in my pipeline
      }
    }
  }

}
