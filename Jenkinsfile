#!/usr/bin/env groovy

node('docker') {
    stage('Build') {
        docker.image('alpine').inside {
            echo 'im building'
            sh 'uname -a'
        }
    }

    stage('Test') {
        docker.image('redis').withRun { container ->
            sh 'ls -lah'
        }
    }

    stage('Deploy') {
    }
}
