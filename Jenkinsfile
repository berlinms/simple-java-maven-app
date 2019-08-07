pipeline {
    agent any
    stages {
        stage('Build program') {
            steps {
                sh 'mvn -B -DskipTests'
            }
        }
    }
}
