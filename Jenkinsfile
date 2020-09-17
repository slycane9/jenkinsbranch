pipeline { 
    agent any 
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') { 
            steps { 
                sh 'echo hi' 
                sh 'pwd'
                sh 'ls ..'
            }
        }
        stage('Test'){
            steps {
                sh 'echo test'
            }
        }
        stage('Deploy'){
            when { tag "submit-*" }
            steps {
                sh 'echo tag detected'
            }
        }
    }
}
