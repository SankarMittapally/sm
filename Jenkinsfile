#!/usr/bin/env groovy
pipeline {
    environment {
                def mvnHome = tool name: 'ApacheMaven', type: 'maven'
                def mvnCMD = "${mvnHome}/bin/mvn"
                }  
    properties([[$class: 'RebuildSettings', autoRebuild: false, rebuildDisabled: false], parameters([string(defaultValue: 'master', description: '', name: 'branch', trim: false)]), pipelineTriggers([])])

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
                   when { 
                        branch 'master'
                        }
                   steps {
                       script {
                            git url: 'https://github.com/SankarMittapally/sm.git', branch: "${params.branch}"
                              }
                          }
         
	}
}
}
