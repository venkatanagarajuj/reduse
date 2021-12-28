// Jenkinsfile
// ----------------------------------------------------------------------
// This is as simple as it gets with declarative pipeline
// ----------------------------------------------------------------------
pipeline {
   agent any
   stages {
      stage('Say Hello') {
         steps {
            checkout([$class: 'GitSCM',
            extensions: [[$class: 'CloneOption', reference: '/var/lib/gitcache/my-repository.git']],
])
         }
      }
   }
}