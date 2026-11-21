pipeline {
agent any
stages {
  stage('Maven Build') { 
  steps { 
  dir ('Amazon') {
  sh 'mvn clean install'
  
  }
  
  
  }

}

post { 
 success { 
 emailext ( 
 to: 'udaykumar.udaykv@gmail.com',
 subject: 'Build execution',
 body: 'Build got success.'
 )
 
 }

}

}
