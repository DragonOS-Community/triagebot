node {
    checkout scm
    def customImage = docker.build("dragonos-triagebot:${env.BUILD_ID}")
    docker.withRegistry('${env.TARGET_REGISTRY_URL}'){
        customImage.push()
    }
}
