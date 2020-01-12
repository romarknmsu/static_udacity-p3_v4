pipeline {
  agent any
  stages {
    stage('Lint HTML') {
      steps {
        s3Upload(bucket: 'static-jenkins-pipeline-romero', pathStyleAccessEnabled: true, payloadSigningEnabled: true, file: 'index.html')
      }
    }

    stage('Upload to AWS') {
      steps {
        s3Upload(bucket: 'static-jenkins-pipeline-romero', pathStyleAccessEnabled: true, payloadSigningEnabled: true)
      }
    }

  }
}