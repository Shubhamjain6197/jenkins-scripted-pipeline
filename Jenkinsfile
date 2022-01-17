pipeline {
    agent {
        label 'Slave-Node'
    }

    stages {
        stage('Git-Checkout') {
            steps {
                echo 'This is an checkout script'
                git branch: 'main', url: 'https://github.com/Shubhamjain6197/jenkins-scripted-pipeline.git'
            }
        }
        stage('Dev') {
            steps {
                echo 'This is an Dev script'
                bat '''py dev.py'''
            }
        }
        stage('Test') {
            steps {
                echo 'This is an Test script'
                bat '''py test.py'''
            }
        }
        stage('Prod') {
            steps {
                echo 'This is an Prod script'
                bat '''py prod.py'''
            }
        }
    }
}
