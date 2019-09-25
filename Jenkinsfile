#!groovy
pipeline {
         agent any
         stages {
            stage('Parameters') {
                steps {
                    script{
                    resp = input message: 'Enter the branch name: ', parameters: [string(defaultValue: 'master',
                    description: 'Enter response', name: 'branchname')]
                    }
                    echo "${resp}"
                }
            }
        
            stage('Build') {
                steps {
                     echo 'Building..'
                     git([url: 'https://github.com/rezadarzi/avihang.git', branch: 'avi-1'])
                     //git([url: 'ssh://root@172.24.25.235/git/avi.git', branch: 'master' ,credentialsId: "0f967e9c-b4d9-49af-8311-268ff7ef9481"])
                     echo "{$BUILD_URL}"
                     buildName "reza"
                     buildDescription "test discription"
                     echo "This test for using Jenkinsfile"
                }
            }
        }
}
