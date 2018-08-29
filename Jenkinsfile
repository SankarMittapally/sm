#!/usr/bin/env groovy
pipeline {
    properties([[$class: 'RebuildSettings', autoRebuild: false, rebuildDisabled: false], parameters([choice(choices: ['master', 'sm1', 'test', 'dev', 'uat'], description: 'Branch Wise Build', name: 'branch')]), pipelineTriggers([])])
    environment {
                def mvnHome = tool name: 'ApacheMaven', type: 'maven'
                def mvnCMD = "${mvnHome}/bin/mvn"
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
          stage ('SCM Checkout') { 
                   steps {
                       script {
                            git url: 'https://github.com/SankarMittapally/sm.git', branch: "${params.branch}"
                              }
                          }
                      
	}
}

