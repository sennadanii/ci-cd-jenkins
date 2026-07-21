pipeline {
    agent any

    tools {
        nodejs 'nodejs'
    }

    stages {
        stage('Instalação das dependências') {
            steps {
                echo 'Instalando os pacotes nodes...'
                bat 'npm install'
            }
        }
        stage('Execução dos testes') {
            steps {
                echo 'Executando os testes...'
                bat 'npm test'
            }
        }
    }

    post {
        success {
            echo'Build e testes executados com sucesso!'
        }
        failure{
            echo 'Falha na execução do pipeline'
        }
    }
}