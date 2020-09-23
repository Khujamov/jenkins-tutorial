pipeline{
    agent any
    stages{
        stage("test"){
            steps{
                echo "========executing test ========"
            }
        }
        stage("build"){
            steps{
                echo "========executing build ========"
            }
        }
        stage("deploy"){
            steps{
                echo "========executing deploy ========"
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}