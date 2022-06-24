pipeline{
    agent any
    emailext body: 'New commits found. Pipeline has been triggered', subject: 'JENKINS- DEMO PROJECT', to: 'chinmayee.trivedi@unthinkable.co'
    stages{
        stage("DEVELOPMENT"){
            steps{
                echo "Executing the development stage"
                
            }
        }
        
        stage("STAGING"){
            steps{
                echo "Executing the staging phase"
            }
        }
        
        stage("TESTING"){
            steps{
                echo "Executing the testing stage"
            }
        }
        
        stage("PRODUCTION"){
            input{
                message "Should we continue?"
                ok "Yes We should!"
            }
            steps{
                echo "Executing the production stage"
            }
        }
    }
    post{
        always{
            echo "========This is jenkins demo project========"
        }
        success{
            echo "========pipeline executed successfully ========"
            emailext body: 'Pipeline created successfully with Build No . ${BUILD_ID}', subject: 'JENKINS- DEMO PROJECT', to: 'chinmayee.trivedi@unthinkable.co'
        }
        failure{
            echo "========pipeline execution failed========"
            emailext body: 'Pipeline creation failed with Build No . ${BUILD_ID}. Please check1', subject: 'JENKINS- DEMO PROJECT', to: 'chinmayee.trivedi@unthinkable.co'
        }
    }
}
