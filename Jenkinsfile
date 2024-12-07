pipeline {
    agent {
        node {
            label "linux && java17"
        }
    }
    stages {
        stage("Build"){
            steps{
                echo("Build")
                sh("./mvnw clean compile test-compile")
                echo("Finish Build")
            }
        }
        stage("Test"){
            steps{
                echo("Test")
                sh("./mvnw test")
                echo("Finish Test")
            }
        }
        stage("Deploy"){
            steps{
                echo("Ini Deploy")
                sleep(20)
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