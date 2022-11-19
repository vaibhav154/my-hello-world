pipeline{
    agent any
    parameters{
        string(name: 'DEPLOY_ENV',defaultValue:'staging',description:'')
        text(name:'DEPLOY_TEXT',defaultValue:'One\nTwo\nThree\n',description:'')
        booleanParam(name:'TOGGLE',defaultValue:'true',description:'Toggle this value')
        choice(name:'CHOICE',choices:['One','Two','Three'],description:'Pick something')
        file(name:'FILE',,description:'Some file to upload')
        password(name:'PASSWORD',defaultValue:'SECRET',description:'A secret password')
    }
    options{
        timestamps()
    }
    stages{
        stage('triggerjob'){
//            options{
//                retry(3)
//                timeout(time:5,unit:'SECONDS')
//            }
            steps{
                build('hello-world')                
//                echo "string $DEPLOY_ENV"
//                sleep(10)
            }
       }
        stage('text'){
            steps{
                echo "text $DEPLOY_TEXT"
            }
       }
        stage('booleanParam'){
            steps{
                script{
                    if(TOGGLE){
                        echo "now execute, boolean is true"
                    }
                    else{
                        echo "Don't execute, boolean is true"
                    }
                }
            }
       }
        stage('choice'){
            steps{
                script{
                    if(DEPLOY_ENV=='staging'){
                        echo "choice $CHOICE"
                    }
                }
            }
       }
        stage('file'){
            steps{
                echo "file $FILE"
            }
       }
        stage('password'){
            steps{
                echo "password $PASSWORD"
            }
       }
    }
}
