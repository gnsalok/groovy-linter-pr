node {
    checkout scm
    docker.image('nvuillam/npm-groovy-lint').inside {
        sh 'npm-groovy-lint'
    }
}