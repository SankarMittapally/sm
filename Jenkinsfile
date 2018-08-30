#!/usr/bin/env groovy
pipeline {
    environment {
                def mvnHome = tool name: 'ApacheMaven', type: 'maven'
                def mvnCMD = "${mvnHome}/bin/mvn"
                def branch_build = 'echo "${env.branch}" |tr -d 'refs/remotes/origin/''
                }  

    agent any
          stages {
          stage ('SCM Checkout') { 
                   steps {
                       script {
                            echo "${branch_build}"
                              }
                          }
         
	}
}
}
