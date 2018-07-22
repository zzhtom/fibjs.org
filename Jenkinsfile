pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''echo "checkout"
zip fibjs.org.zip ./*'''
        archiveArtifacts(artifacts: 'fibjs.org.zip', fingerprint: true, onlyIfSuccessful: true, allowEmptyArchive: true)
      }
    }
  }
}