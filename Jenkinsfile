pipeline{
    agent any
    parameters {
        booleanParam(name: 'executeTests', defaultValue: true, description:'')
    }
    stages{
        stage("init"){
            gv = load "script.groovy"
        }
        stage("test"){
            when {
                expression {
                    params.executeTests
                }
            }
            steps{
                gv.testApp()
            }
        }
        stage("build"){
            steps{
                echo "========executing build ========"
                gv.buildApp();
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