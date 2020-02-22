pipeline{

agent any
      environment{
         FOO = "bar"
         }
      options{
             timestamps()
             
           }
      stages{
             stage('Build'){
                  when {
                      environment name: "FOO", value: "bar"
                       }
                  options{
                        timeout(time: 1, unit: "MINUTES")
                       }
                  steps{
                     echo  "some code compilation"
                      sh 'printf "\\[31mSome Code compilation here.....\\e[0m\\n"'
                    
                      }
                  }
              stage('Test'){
                    options{
                         timeout(time: 2, unit: "MINUTES")
                         }
                    steps{
                      echo " some tests execution here "
                      sh 'printf "\\e[31Some tests execution here.... \\e[0m\\n"'
                      }

                      
                    }
               stage("Reading Env variables"){
                   echo " the build number is ${env.BUILD_NUMBER}"
                   echo " you can also use \${BUILD_NUMBER} -> ${BUILD_NUMBER}"
                   sh 'echo "I can access $BUILD_NUMBER in shell command as well."'
                  }

             }
        }       

                  
