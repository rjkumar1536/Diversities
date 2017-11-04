/*def notifySlack(String Status = 'STARTED',String customMessage=" ")

{

    // build status of null means successful

    Status =  Status ?: 'SUCCESSFUL'



    // Default values

    def colorName = 'RED'

    def colorCode = '#FF0000'

    def subject = "${Status}: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'"

    def summary = "${subject} (${env.BUILD_URL})"

    def details = """<p>STARTED: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]':</p>

    <p>Check console output at <a href="${env.BUILD_URL}">${env.JOB_NAME} [${env.BUILD_NUMBER}]</a></p>"""

     

    // Override default values based on build status

    if (Status == 'STARTED') {

        color = 'YELLOW'

        colorCode = '#FFFF00'

    }

    else if (Status == 'SUCCESSFUL'){

        color = 'GREEN'

        colorCode = '#00FF00'

    }

    else {

        color = 'RED'

        colorCode = '#FF0000'

    }

    slackSend (color: colorCode, message: summary)

    slackSend (color: colorCode, message: customMessage)
            
}*/
node {
            env.WorkSpace = 'C:\\Users\\Administrator\\Desktop'
            dir("${env.WorkSpace}") {

                stage 'CHECKOUT'

                try{           

                     //checkout([$class: 'GitSCM', branches: [[name: 'origin/' + ""]], doGenerateSubmoduleConfigurations: false,  extensions: [[$class: 'PruneStaleBranch']], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/rjkumar1536/Demo.git']]])
                      checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '56506a35-9c43-4e38-acf6-96cc65436690', url: 'https://github.com/rjkumar1536/Demo.git']]])
                }

                catch(Exception ex){

                    throw ex

                }     
                
                stage 'BUILD'

                try {

                    //notifySlack('STARTED')

                    echo "hello"

                } 

                catch (Exception ex){


                    echo "There is some error in build"

                    currentBuild.result = "FAILED"

                    throw ex

                }
            }
}

