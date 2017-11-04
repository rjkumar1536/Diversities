node {
            env.WorkSpace = 'C:\\Users\\Administrator\\Desktop'
            dir("${env.WorkSpace}") {

                stage 'CHECKOUT'

                try{           

                     //checkout([$class: 'GitSCM', branches: [[name: 'origin/' + ""]], doGenerateSubmoduleConfigurations: false,  extensions: [[$class: 'PruneStaleBranch']], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/rjkumar1536/Demo.git']]])
                      checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '56506a35-9c43-4e38-acf6-96cc65436690', url: 'https://github.com/rjkumar1536/Demo.git']]]
                }

                catch(Exception ex){

                    throw ex

                }     
            }
}

