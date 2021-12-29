// Jenkinsfile
// ----------------------------------------------------------------------
// This is as simple as it gets with declarative pipeline
// ----------------------------------------------------------------------
pipeline {
    environment {
     reponame = "hello-world"
     repo_url = "https://github.com/venkatanagarajuj/reduse.git"
   }
    agent any
    stages {
        stage('Example Build') {
            steps {
               
                checkout([$class: 'GitSCM',
                branches: [[name: 'master']],
                doGenerateSubmoduleConfigurations: false,
    extensions: [ [$class: 'RelativeTargetDirectory', relativeTargetDir: reponame], [$class: 'CloneOption', reference: '/var/lib/gitcache']],
                userRemoteConfigs: [[credentialsId: 'none', url: repo_url]
                sh "set files"
        ]

])
            }
        }
    }
}
