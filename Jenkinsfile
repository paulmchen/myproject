#!/usr/bin/env groovy

pipeline {
    agent { docker 'maven:3.3.3' }
    stages {
        stage('package') {
            steps {
                sh 'mvn --version'
                echo 'Install, build and package ...'
                sh 'mvn package'
            }
        }
        stage('test') {
            steps {
                echo 'Testing ...'
                sh 'mvn test'
            }
        }
    }
}