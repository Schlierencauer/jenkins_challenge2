pipeline{
    agent any
    stages{
        stage('Calculate Pi') {
            steps{
                sh "chmod +x ./algorithm.sh"
                sh "./algorithm.sh > report.txt"
                
                archiveArtifacts allowEmptyArchive: true, 
                artifacts: '*.txt', 
                fingerprint: true, 
                followSymlinks: false, 
                onlyIfSuccessful: true
            }
        }
    }
}
