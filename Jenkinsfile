// Jenkinsfile
// ----------------------------------------------------------------------
// This is as simple as it gets with declarative pipeline
// ----------------------------------------------------------------------
pipeline {
    environment {
     reponame = "hello-world"
   }
    agent any
    stages {
        stage('Example Build') {
            steps {
                git 'https://github.com/venkatanagarajuj/reduse.git'
                sh 'git fetch --no-tags --force --progress -- https://github.com/venkatanagarajuj/reduse.git +refs/heads/*:refs/remotes/origin/*'
               checkout([$class: 'GitSCM', branches: [[name: '**']], 
doGenerateSubmoduleConfigurations: false, 
extensions: [[$class: 'CheckoutOption', timeout: 20],
 [$class: 'BuildChooserSetting', buildChooser: [$class: 'GerritTriggerBuildChooser']], 
 [$class: 'CloneOption', honorRefspec: true, noTags: true, reference: '', timeout: 20]], 
 submoduleCfg: [], userRemoteConfigs: [[refspec: '$GERRIT_REFSPEC', url: 'git:https://github.com/venkatanagarajuj/reduse.git']]])
            }
        }
    }
}
