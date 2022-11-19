pipeline{
   agent any 
   options{
          timestamps()
   }
   stages{
        stage('build'){
            steps{
                build('hello-world')
                 echo "Hello world"
            }       
        }
    }
}