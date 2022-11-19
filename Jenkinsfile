pipeline{
   agent any 
   options{
          timestamps()
   }
   stages{
        stage('build'){
            parallel{
                stage('job1'){
                    steps{
                        echo "this is job1"
                        sleep(5)
                        echo "job1 resumes after 5 seconds pause"
                        sleep(5)
                    }
                }
                stage('job2'){
                    steps{
                        echo "This is job2 taking 4 seconds pause"
                        sleep(5)
                        echo "job2 is completed within span of 5 seconds"
                    }
                }
            }
        }
    }   
}
