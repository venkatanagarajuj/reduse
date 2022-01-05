// Jenkinsfile
// ----------------------------------------------------------------------
// This is as simple as it gets with declarative pipeline
// ----------------------------------------------------------------------
pipeline {
    environment {
     reponame = "reduse"
   }
    agent any
    stages {
        stage('Example Build') {
            steps {
               checkout_from_reference("master")
            }
        }
    }
}

def checkout_from_reference(commit) {
    def reponame = "reduse"
    def repo_url = "https://github.com/venkatanagarajuj/reduse.git"
 
    echo "Checkout SHA from reference $commit"
    checkout([
        $class: 'GitSCM',
        branches: [[name: commit]],
        doGenerateSubmoduleConfigurations: false,
        extensions: [
            [$class: 'RelativeTargetDirectory', relativeTargetDir: reponame],
            [$class: 'CloneOption', reference: "/opt/${reponame}"]
        ],
        submoduleCfg: [],
        userRemoteConfigs: [
            [url: repo_url]
        ]
    ])
    // just to show we are in the right commit:
    dir(reponame) {
        sh(script: "git rev-parse HEAD")
    }
}
