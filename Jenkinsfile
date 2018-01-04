
pipeline
{

agent any
  stages{
    stage{'Compile Stage'){
      steps{
      withmaven(maven:'maven3')
        sh 'mvn clean compile'
      }
    }
         }
    stage('Testing stage"){
          steps{
            withmaven(maven:'maven3')
          }
          }
          }
          satge('deployment stage')
          steps{
            withmaven(maven:'maven3')
          
 
    } 
  }
}
}
