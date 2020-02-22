pipeline{

agent any
      options{
             timestamps()
             ansiColor("xterm")
           }
      stages{
             stage('Build'){
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

             }
        }       

                  
