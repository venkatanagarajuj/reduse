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
                git 'https://github.com/ravdy/hello-world.git'
                checkout([$class: 'GitSCM',
                branches: [[name: '*/master']],
                doGenerateSubmoduleConfigurations: false,
    extensions: [ [$class: 'RelativeTargetDirectory', relativeTargetDir: hello-world], [$class: 'CloneOption', reference: '/var/lib/gitcache']],
])
            }
        }
    }
}
