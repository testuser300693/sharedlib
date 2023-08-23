@Library('sharedLib')_

import com.stageclasses.SampleClass

node {
    try {
        stage('Demo') {
            echo 'Hello world'
            sayHello 'Alex'
        }
        stage('callclass') {

            script {
                def pipelineHelper = new SampleClass()
                // pipelineHelper.stageCheckout
                pipelineHelper.age = 21
                pipelineHelper.increaseAge(10)
                echo 'Incremented age, is now : ' + person.age
            }
            
        }
    } catch (Exception e) {
        currentBuild.result = 'FAILURE'
        echo "An error occurred: ${e.getMessage()}"
        error("Pipeline failed due to an error.")
    }
}
