node('built-in')

{

stage('Continuous Download') 
   
	 {
	
    git 'https://github.com/tkeesara/maven.git'
    
	}

stage('Continuous build') 
   
	 {
	
   sh label: '', script: 'mvn package'
	}

stage('Continuous Deployment') 
   
	 {
	
 sh label: '', script: 'scp  /home/ubuntu/.jenkins/workspace/scriptedpipeline/webapp/target/webapp.war  ubuntu@172.31.35.34:/var/lib/tomcat9/webapps/qaenv.war'
	}
}
}
