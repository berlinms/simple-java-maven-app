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
                
                  nexusPublisher nexusInstanceId: 'LocalNexus', nexusRepositoryId: 'releases', packages: [[$class: 'MavenPackage', mavenAssetList: [[classifier: '', extension: '', filePath: 'war/target/jenkins.war ']], mavenCoordinate: [artifactId: 'jenkins-war', groupId: 'org.jenkin-ci.main', packaging: 'war', version: '2.22']]]
            }
            } 
            }    
            
}
