node {
            env.WorkSpace = 'C:\\Users\\Administrator\\Desktop'
            dir("${env.WorkSpace}") {

                stage 'CHECKOUT'

                try{           

                    def prdetails = "${env.BRANCH_NAME}".split("-")

                    checkout([$class: 'GitSCM', branches: [[name: 'origin/' + "${env.BRANCH_NAME}"]], doGenerateSubmoduleConfigurations: false,  extensions: [[$class: 'PruneStaleBranch']], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/rjkumar1536/Demo.git']]])

                    // checkout([$class: 'GitSCM', branches: [[name: 'origin/pull/'+prdetails[1]+'/head']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[name: 'origin', refspec: '+refs/pull/'+prdetails[1]+'/head:refs/remotes/origin/pull/'+prdetails[1]+'/head', url: 'git@github.com:carwale/CIDemoRepository.git']]])

                }

                catch(Exception ex){

                    throw ex

                }     
            }
}

