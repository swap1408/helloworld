node {
    stage('Preparation') {
        git branch: 'master', url: 'https://github.com/swap1408/helloworld.git'
    }
    stage('Build') {
                sh 'mvn clean package'
            }
    stage('ArchiveResults') {
        archiveArtifacts '**/*.war'
    }
}
