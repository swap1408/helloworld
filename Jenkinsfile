node () {
    checkout scm
    def a = load('a.groovy')
    echo("${env.BUILD_NUMBER}")
    echo("${a.LOADED_BUILD_NUMBER}")
    stage(Preparation) {
        git branch: 'master', url: 'https://github.com/swap1408/helloworld.git'
    }
    stage('Build') {
                sh 'mvn clean package'
            }
    stage('ArchiveResults') {
        archiveArtifacts 'target/*.war'
    }
}
