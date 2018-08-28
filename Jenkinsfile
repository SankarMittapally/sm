pipeline{
    agent any
   
   stages{
       stage('SCM CheckOut'){
	       steps{  
	           git 'https://github.com/SankarMittapally/sm.git'
		        }
			}
	stage('Mvn Package'){
	    steps{
	        def mvnHome = tool name: 'ApacheMaven', type: 'maven'
                def mvnCMD = "${mvnHome}/bin/mvn"
		sh "${mvnCMD} clean compile"
			}
	}
}
}
