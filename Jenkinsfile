#!/usr/bin/env groovy
pipeline {
    environment {
                def mvnHome = tool name: 'ApacheMaven', type: 'maven'
                def mvnCMD = "${mvnHome}/bin/mvn"
                }
    parameters {
            string(
                name: 'branch',
                defaultValue:"master",
                description: "Where to put the build!")
    }  

    agent any
          stages {
          stage ('SCM Checkout') { 
                   steps {
                       script {
                            echo "${branch}"
                              }
                          }
         
	}
}
}
