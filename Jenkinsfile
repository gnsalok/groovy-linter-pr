pipeline{

    agent any

    stages{
    // Lint with Mega-Linter: https://nvuillam.github.io/mega-linter/
        stage('Mega-Linter') {
            agent {
                docker {
                    label 'docker'
                    image 'nvuillam/mega-linter:v4'
                    args "-e VALIDATE_ALL_CODEBASE=true -v ${WORKSPACE}:/tmp/lint --entrypoint=''"
                    reuseNode true  
                }
            }
            steps {
                sh '/entrypoint.sh'
            }
        }
    }

}
