pipeline {
parameters {
 string (name :'version', description: 'the newest version' )
choice (name:'mychoice' , choices:['1.0','1.1','1.2'] )

 }
 agent any
  stages {
    stage('parameters') {
      steps  {
      echo "Iam ${params.mychoice} ${params.version} " // Now I can use docker commands in my pipeline
      }
    }
  }

}
