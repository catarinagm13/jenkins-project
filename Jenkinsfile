pipeline{
    agent any
    stages{
    stage('Parallel'){
        parallel {
            stage ('Criando file.txt') {
                steps{
                    writeFile file: '/var/jenkins_home/workspace/pipeline-jenkins/file.txt', text: 'Texto do file.txt'
                }
            }
            stage('Criando meuarquivo.txt'){
                steps{
                writeFile file: '/var/jenkins_home/workspace/pipeline-jenkins/meu-arquivo.txt', text: 'Texto do meuarquivo.txt'
                }
            }
        }
    }
    stage('Criacao do zip'){
        steps {
            zip zipFile: 'teste.zip', archive: false, dir: '/var/jenkins_home/workspace/pipeline-jenkins/'
            archiveArtifacts artifacts: 'teste.zip', fingerprint: true
        }
    }
    }
}

