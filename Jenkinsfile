pipeline  {
  agent any
  stages{
    stage('Build'){
      steps {
        sh 'g++ hello.cpp -o hello_exec'
        echo 'Build Stage Successful'
      }
    }
    stage('Test'){
      steps {
        sh './hello_exec'
        echo 'Test Stage Successful'
      }
    }
    stage('Deploy'){
      steps{
        echo 'Deployment done'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
