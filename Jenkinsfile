pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''echo "checkout"
zip fibjs.org.zip ./*'''
        archiveArtifacts(artifacts: 'fibjs.org.zip', fingerprint: true, onlyIfSuccessful: true, allowEmptyArchive: true)
	sshPublisher(publishers: [sshPublisherDesc(configName: 'zzh', transfers: [sshTransfer(excludes: '', execCommand: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '', sourceFiles: 'fibjs.org.zip')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
      }
    }
  }
}
