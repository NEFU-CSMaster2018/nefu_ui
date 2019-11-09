pipeline {
    agent {
        docker {
            image 'node:latest'
        }
    } 
    stages {
        stage('clean') {
            steps {
                echo 'start to clean'
                sh 'rm -rf dist'
            }
        }
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
                echo '暂时软连接到本机'
           }
        }
    }
}