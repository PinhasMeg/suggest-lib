pipeline {

    agent any

    tools{
        maven "maven-3.6.2"
    }


    


    stages{
        
        
        
        stage('checkout'){
            steps{
                
                deleteDir()
                checkout scm
                }
        }
                

        stage ('Build ') {
            steps {
                withMaven(jdk: 'jdk-8', maven:'maven-3.6.2') {
                sh'''echo 'BUILDING' '''
                
                //sh" echo ${env.GIT_BRANCH} "
                
                sh "mvn package"

                sh"mvn deploy"


                } 
            }
        }
    }
            
        
}





