node{
     git branch: 'main', url: 'git@github.com:khaledhawil/simple-java-app.git'
     stage('build'){
          try{
              sh'echo "Build Stage"' 
          }
          catch(Exception e){
               sh'echo "Build Stage Failed"'
              throw e
          }
     }

     stage('test'){
          if(env.BRANCH_NAME == "feat"){
               sg'echo "Test Stage"'
          }
          else{
               sh'echo "Test Stage Skipped"'
          }
     }

     stage('deploy'){
          if(env.BRANCH_NAME == "main"){
               sh'echo "Deploy Stage"'
          }
          else{
               sh'echo "Deploy Stage Skipped"'
          }
     }
}