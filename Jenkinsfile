pipeline{
    agent any
    stages{
        stage('Calculate Pi') {
            steps{
                sh "./algorithm.sh > report.txt"
                
                archiveArtifacts allowEmptyArchive: true, 
                artifacts: '', 
                fingerprint: true, 
                followSymlinks: false, 
                onlyIfSuccessful: true
            }
        }
    }
}
