#!/usr/bin/env groovy
pipeline {
    environment {
                def mvnHome = tool name: 'ApacheMaven', type: 'maven'
                def mvnCMD = "${mvnHome}/bin/mvn"
                }  
    agent any
    stages {
         stage ('SCM CheckOut') {
             steps {  
                 git 'https://github.com/SankarMittapally/sm.git'
                   }
           }
	 stage ('Mvn Package') {
	     steps {
		sh "${mvnCMD} clean compile"
		}
	}
     }
}
