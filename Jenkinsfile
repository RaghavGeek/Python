pipeline {
       agent any
   stages {
    stage('Initialize'){
      steps{
        echo "We are doing some test"
        echo "PATH = ${PATH}"
        }
    }
    stage('Build'){
           steps
           {
        sh 'pip install -r requirements.txt'          
        sh "python server.py"
    }     
    }
  }
}
