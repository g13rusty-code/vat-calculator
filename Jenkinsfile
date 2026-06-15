pipeline {
    agent any

    stages {
       
        }
        stage('Run Tests') {
            steps {
              sh 'npm install'
              sh 'CI=true npm test'
           }
        }
        stage('Build Webpack') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Archive') {
            steps {
              sh 'tar -czf build.tar.gz build'
              archiveArtifacts 'build.tar.gz'
            }
        }
    }
}
