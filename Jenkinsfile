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
                checkout([$class: 'GitSCM',
                branches: [[name: 'master']],
                doGenerateSubmoduleConfigurations: false,
    extensions: [ [$class: 'RelativeTargetDirectory', relativeTargetDir: reponame], [$class: 'CloneOption', reference: '/var/lib/gitcache']],
])
            }
        }
    }
}
