node('docker') {
    def dockerPython

    stage('Clone repository') {
        checkout scm
    }

    stage('Build docker-python agent') {
        dockerPython = docker.build("davydstoppel/jenkins-docker-python-agent", "docker-python")
    }

    stage('Push docker-python image') {
        dockerPython.push("latest")
    }
}
