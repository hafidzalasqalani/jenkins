pipeline {
    agent {
        node {
            label "linux && java17"
        }
    }
    stages {
        stage("Hello"){
            steps{
                echo("Halo")
            }
        }
    }
    post{
        always{
            echo "done"
        }
    }
}