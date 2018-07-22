pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo "checkout"'
        archiveArtifacts(artifacts: 'package.json', fingerprint: true, onlyIfSuccessful: true, allowEmptyArchive: true)
      }
    }
  }
}