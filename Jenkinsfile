node {
            env.WorkSpace = 'C:\\Users\\Administrator\\Desktop'
            dir("${env.WorkSpace}") {

                stage 'CHECKOUT'

                try{           


                     //checkout([$class: 'GitSCM', branches: [[name: 'origin/' + ""]], doGenerateSubmoduleConfigurations: false,  extensions: [[$class: 'PruneStaleBranch']], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/rjkumar1536/Demo.git']]])
                      checkout([$class: 'GitSCM', branches: [[name: '/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '56506a35-9c43-4e38-acf6-96cc65436690', url: 'https://github.com/rjkumar1536/Demo.git']]])
                    // checkout([$class: 'GitSCM', branches: [[name: 'origin/pull/'+prdetails[1]+'/head']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[name: 'origin', refspec: '+refs/pull/'+prdetails[1]+'/head:refs/remotes/origin/pull/'+prdetails[1]+'/head', url: 'git@github.com:carwale/CIDemoRepository.git']]])
                     
                }

                catch(Exception ex){

                    throw ex

                }     
            }
}

