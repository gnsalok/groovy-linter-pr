pipeline{
    agent any 
    stages{
    // Lint with Mega-Linter: https://nvuillam.github.io/mega-linter/
        stage('Mega-Linter') {
            when{
                branch 'master'
            }
            agent {
                docker {
                    image 'nvuillam/mega-linter:v4'
                    args "-e VALIDATE_ALL_CODEBASE=true -v ${WORKSPACE}:/tmp/lint --entrypoint=''"
                    reuseNode true
                }
            }
                steps {
                   echo 'Linting Mega Linter'
                }
        }
    }

}
