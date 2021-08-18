pipeline{
    agent any
    tools{
        maven ('maven3')
    }
    stages{
        stage('Maven Build'){
            steps{
                sh 'mvn clean package'
            }

        }

        stage('Upload to nexus'){
            steps{
               nexusArtifactUploader artifacts: [[artifactId: 'myweb', 
               classifier: '', file: 'myweb-0.0.1-SNAPSHOT.war', 
               type: 'war']], credentialsId: 'nexus3', groupId: 'in.javahome', 
               nexusUrl: '172.31.39.176:8081', nexusVersion: 'nexus3', 
               protocol: 'http', repository: '13.233.143.191', version: '0.0.1-SNAPSHOT' 
            }

        }

    }

}
