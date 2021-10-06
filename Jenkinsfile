@Library('shared-library-a') _
pipeline {
    agent any
    environment {
        DOCKER_CRED = 'dockerhub'
    }
    stages {
        stage("Checkout code") {
            steps {
                checkOut()
            }
        }
        stage("Build image") {
            steps {
                script {
                    step.npmBuild()
                }
            }
        }
        stage("Push image") {
            steps {
                script {
                    step.pushImage()
                    }
                }
            }
          }       
        }
