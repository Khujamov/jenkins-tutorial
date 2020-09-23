pipeline{
    agent any
    parameters {
        booleanParam(name: 'executeTests', defaultValue: true, description:'')
    }
    stages{
        stage("test"){
            when {
                expression {
                    params.executeTests
                }
            }
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