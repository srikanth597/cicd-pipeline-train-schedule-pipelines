pipeline{
  agent any;

  stages{
    stage('build'){
      steps{
        echo 'Hii';
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
