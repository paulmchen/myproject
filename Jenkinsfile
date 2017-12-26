#!/usr/bin/env groovy

pipeline {
    agent { docker 'maven:3.3.3' }
    stages {
        stage('package') {
            steps {
                sh 'mvn --version'
                echo 'Building ...'
                sh 'mvn install'
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