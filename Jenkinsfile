pipeline {
    agent {
        node {
            label "linux && java17"
        }
    }
    stages {
        stage("Build"){
            steps{
                echo("Ini Build")
            }
        }
        stage("Test"){
            steps{
                echo("Ini Test")
            }
        }
        stage("Deploy"){
            steps{
                echo("Ini Deploy")
            }
        }
    }
    post{
        always{
            echo "done"
        }
        success{
            echo "done"
        }
        failure{
            echo "done"
        }
        cleanup{
            echo "done"
        }
    }
}