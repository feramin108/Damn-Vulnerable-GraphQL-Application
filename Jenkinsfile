Pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('build'){
            step{
                sh 'make'
            }
        }
        stage('Test'){
            step{
                sh 'make check'
                junit 'reports/**/*.xml'
            }
        }
        stage('deploy'){
            step{
                sh 'make publish'
            }
        }
    }
}