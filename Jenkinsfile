pipeline{
  agent any;
  
  stages{
    stage('build'){
      when{
        branch 'patch-1'
      }
      steps{
        echo 'Hii';
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
        script{
        scp dist/trainSchedule.zip cloud_user@3.110.103.181:/home/cloud_user/
         }
      }
    }
  }
}
