pipeline{
    agnet any
    stages{
        stage('Build'){
            steps{
                sh 'mvn clean package'
            }
            post{
                success{
                    echo "NOW Archiving....."
                    archiveArtifacts artifacts:'**/target/*.war'
                }
            }
        }
    }
}