pipeline {
         agent { docker { image 'python:3.7.2' } }
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
    }     
    }
   stage('Sonar'){
                steps
                {
        
            sh "sonar-scanner -Dsonar.projectKey=PythonProject -Dsonar.sources=. -Dsonar.host.url=http://52.143.7.186/sonarqube-1336430 -Dsonar.login=587c3100c0a7abe49cc26823506555469c971a10"
        
                }
     }

  }
}
