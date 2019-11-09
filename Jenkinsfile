pipeline {
    agent {
        docker {
            image: 'node:latest'
        }
    } 
    stages {
        stage('build') {
            echo 'start to build'
            sh 'npm run build'
        }
        stage('publish') {
            echo 'start to publish ...'
            sh 'rm -rf /home/publish-workspace/ui/dist'
            sh 'mv ./dist /home/publish-workspace/ui/'
        }
    }
}