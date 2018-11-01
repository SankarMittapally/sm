#!/usr/bin/env groovy
pipeline {
    environment {
                def mvnHome = tool name: 'ApacheMaven', type: 'maven'
                def mvnCMD = "${mvnHome}/bin/mvn"
<<<<<<< HEAD
                def branch_build = 'echo "${env.branch}" |tr -d 'refs/remotes/origin/''
=======
                def branch = 'echo "${env.branch}" |tr -d 'origin/''
>>>>>>> parent of 40f1037...  test
                }  

    agent any
          stages {
          stage ('SCM Checkout') { 
                   steps {
                       script {
<<<<<<< HEAD
<<<<<<< HEAD
                            echo "${branch_build}"
=======
                            git url: 'https://github.com/SankarMittapally/sm.git', branch: "${branch}"
                            sh "${mvnCMD} clean compile"
>>>>>>> parent of ef8d9f3...  adding branch wise build
=======
                            git url: 'https://github.com/SankarMittapally/sm.git', branch: "${branch}"
                            echo "${branch}"
>>>>>>> parent of 40f1037...  test
                              }
                          }
         
	}
}
}
