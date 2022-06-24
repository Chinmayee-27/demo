pipeline{
    agent any
      emailext body: 'A Test EMail', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Test'
        }
    }
}

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
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
