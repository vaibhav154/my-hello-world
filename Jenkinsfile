pipeline{
   agent any 
   options{
          timestamps()
   }
   stages{
        stage('build'){
            steps{
                build(job:"jenkins-parametrized-job",
                parameters:
                [string(name:'Nodes',value:"Linux"),
                string(name:'Versions',value:"4.4"),
                string(name:'Path',value:"/home/saurabh/builds/")])

                 echo "Hello world"
            }       
        }
    }
}