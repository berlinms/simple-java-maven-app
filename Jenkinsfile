pipeline {
    agent any 
    stages {
        stage('build ') {
            steps {
                sh 'mvn clean'
            }
        }
        stage("publish") {
            steps {
                
                 nexusPublisher nexusInstanceId: 'LocalNexus', nexusRepositoryId: 'releases', packages: [[$class: 'MavenPackage', mavenAssetList: [], mavenCoordinate: [artifactId: 'my-app', groupId: 'com.mycompany.app', packaging: 'war', version: '1.0']]]
            }
            } 
            }    
            
}
