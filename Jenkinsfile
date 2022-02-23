pipeline{

    agent any

//oving /* and */ to enable. Give name that we gave in global tool configuration in manage jenkins
    tools{
       nodejs 'nodejs' 
    }
   

    stages{
        stage('compile'){
            steps{
                echo 'this is the compile the app job'
                sh 'npm install'
              //  sleep 4 (not required)
            }
        }
        stage('test'){
            steps{
                echo 'this is the test the app job'
                sh 'npm test'
               // sleep 9
            }
        }
        stage('package'){
            steps{
                echo 'this is the package the app job'
                sh 'npm run package'
              //  sleep 7
            }
        }
    }
    
    post{
        always{
            echo 'SUCCESS! this pipeline has completed...'
        }
        
    }
    
}
