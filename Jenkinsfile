pipeline {
    agent any
    tools{
        maven 'mymaven'
    }
    stages {
        stage('Clone Repo') {
            steps {
              git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        stage('Code Review') {
            steps {
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
                    sh "mvn pmd:pm"
                }
            }
        }
        stage('test Code') {
            steps {
                 catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
                sh 'mvn test'
            }
        }
    }
}
}
