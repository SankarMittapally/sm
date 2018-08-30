#!/usr/bin/env groovy
pipeline {
    environment {
                def mvnHome = tool name: 'ApacheMaven', type: 'maven'
                def mvnCMD = "${mvnHome}/bin/mvn"
                def branch_build = 'echo "${env.branch}" |tr -d 'origin/''
                }  

    agent any
          stages {
          stage ('SCM Checkout') { 
                   steps {
                       script {
                            git url: 'https://github.com/SankarMittapally/sm.git', branch: "${branch_build}"
                            echo "${branch_build}"
                              }
                          }
         
	}
}
}
