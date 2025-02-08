node{
     git branch: 'master', url: 'https://github.com/khaledhawil/simple-java-app.git'
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

}