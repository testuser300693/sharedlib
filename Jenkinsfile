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
                def pipelineHelper = new PipelineHelper()
                pipelineHelper.stageCheckout
            }
            
        }
    } catch (Exception e) {
        currentBuild.result = 'FAILURE'
        echo "An error occurred: ${e.getMessage()}"
        error("Pipeline failed due to an error.")
    }
}
