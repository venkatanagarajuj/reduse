// Jenkinsfile
// ----------------------------------------------------------------------
// This is as simple as it gets with declarative pipeline
// ----------------------------------------------------------------------
pipeline {
   agent any
   stages {
      stage('Say Hello') {
            steps {
                git 'https://github.com/venkatanagarajuj/reduse.git'
                checkout([$class: 'GitSCM',
                branches: [[name: 'master']],
                doGenerateSubmoduleConfigurations: false,
    extensions: [ [$class: 'RelativeTargetDirectory', relativeTargetDir: hello],
      	[$class: 'CloneOption', reference: '/var/lib/gitcache']],
])
            }
      }
   }
}
