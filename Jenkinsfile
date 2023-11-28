pipeline {
 agent any
   tools {
     nodejs 'v10.19.0'
  }
stages {
 stage('check'){
steps {
git credentialsId: '123', url: 'https://github.com/prajyotigokhare/juiceshopjenkinspipelinemain.git'
 }
   }
stage('build'){
  steps {
     sh 'npm install'
  }
  }
    stage('Snyk')
  {
 steps {
     snykSecurity snykInstallation: 'snyk', snykTokenId: 'snykid'
     }
  }
}
}
