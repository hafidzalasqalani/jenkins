pipeline {
    agent none
    environment{
        AUTHOR = "Nama"
    }
    stages {
        stage("Prepare"){
                agent {
        node {
            label "linux && java17"
        }
    }
            steps{
                echo("Author ${AUTHOR}")
                echo("Start job : ${env.JOB_NAME}")
                echo("Start build : ${env.BUILD_NUMBER}")
                echo("Start Name : ${env.BRANCH_NAME}")
            }
        }
        stage("Build"){
                agent {
        node {
            label "linux && java17"
        }
    }
            steps{
                echo("Build")
                sh("./mvnw clean compile test-compile")
                echo("Finish Build")
            }
        }
        stage("Test"){
                agent {
        node {
            label "linux && java17"
        }
    }
            steps{
                script{
                    def data = [
                        "firstName": "depan",
                        "lastName": "belakang"
                    ]
                    writeJSON(file: "data.json", json: data)
                }

                echo("Test")
                sh("./mvnw test")
                echo("Finish Test")
            }
        }
        stage("Deploy"){
                agent {
        node {
            label "linux && java17"
        }
    }
            steps{
                script{
                    for (int i=0; i < 10; i++) {
                        echo("Script ${i}")
                    }
                }
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