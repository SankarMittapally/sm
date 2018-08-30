#!/usr/bin/env groovy
pipeline {
    environment {
                def mvnHome = tool name: 'ApacheMaven', type: 'maven'
                def mvnCMD = "${mvnHome}/bin/mvn"
                def branch = 'echo "${env.branch}" |tr -d 'origin/''
                }  

    agent any
//         if (env.BRANCH_NAME == 'master') { 
//         stage ('master') {
//                echo "Master Branch"
//               }
//         stage ('sm1') {
//                echo "SM1 Branch"
//               }
//         }
//         stage ('SCM CheckOut') {
//             steps {  
//                 git 'https://github.com/SankarMittapally/sm.git'
//                   }
//           }
//	 stage ('Mvn Package') {
//	     steps {
//		sh "${mvnCMD} clean compile"
//		}
          stages {
          stage ('SCM Checkout') { 
                   steps {
                       script {
                            git url: 'https://github.com/SankarMittapally/sm.git', branch: "${branch}"
                            echo "${branch}"
                              }
                          }
         
	}
}
}
