@Library('sharedLib')_
node {
    try {
        echo 'Hello world'
        sayHello 'Alex'
    } catch (Exception e) {
        currentBuild.result = 'FAILURE'
        echo "An error occurred: ${e.getMessage()}"
        error("Pipeline failed due to an error.")
    }
}
