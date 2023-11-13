pipeline {
parameters {
 string (name :'version',defaultValue:'Iam god ', description: 'the newest version' )
choice (name:'mychoice' , choices:['1.0','1.1','1.2'] )

 }
 agent any
  stages {
    stage('parameters') {
      steps  {
     script{
      def scr=load "script.groovy"
      echo scr()
     }
      }
    }
  }

}
