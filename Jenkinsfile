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
  stage('Maven Deploy') { 
  steps { 
    sh '''
	
	ls -lh Amazon/Amazon-Web/target/
            cp Amazon/Amazon-Web/target/Amazon.war /home/uday/tomcat1/tomcat1/webapps/
   '''
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

