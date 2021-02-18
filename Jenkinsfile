pipeline {
    agent { dockerfile true }

    parameters {
        string(name: 'node', defaultvalue: "node", description: 'imagem node')
    }

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t node .' 
            }
        }
        stage('Run') {
            steps {
                sh 'docker run -d -p 3000:3000 node'
            }
        }
    }
}
