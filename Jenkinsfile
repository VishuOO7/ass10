pipeline{
  environment{
    reg = "vishuoo7/ass10
    regCre = "docker_id"
    dockerImg = ""
  }
  agent any
  stages{
    stage('Build Image'){
      steps{
        script{
          dockerImg = docker.build reg + ":$BUILD_NUMBER"
        }
      }
    }
    stage('Deploy the image'){
      steps{
        script{
          dockerImg.push()
        }
      }
    }
  }
}
}
