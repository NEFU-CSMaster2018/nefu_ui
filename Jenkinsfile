pipeline {
    agent {
        docker 'node:latest'
    } 
    stages {
        stage('build') {
            steps {
                echo 'start to build'
                sh 'npm config set registry https://registry.npm.taobao.org'
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('publish') {
           steps {
                echo 'start to publish ...'
                sh 'rm -rf /home/publish-workspace/ui/dist'
                sh 'mv ./dist /home/publish-workspace/ui/'
           }
        }
    }
}