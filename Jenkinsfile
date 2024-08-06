#!/usr/bin/env groovy
timeout(time: 30, unit: 'MINUTES') {
    parallel 'docker-validate': {
        node('jenkins-docker-build-node-INV-2750') {
            stage('checking shell') {
                sh '''
                 whoami
                 echo $SHELL
                 docker compose version 
                '''
            }
            stage('checking shell bash') {
                sh '''#!/bin/bash
                 whoami
                 echo $SHELL
                 docker compose version 
                '''
            }
        }
    }
}
