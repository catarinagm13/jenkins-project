pipeline {
    agent any

    parameters {
        string(name: 'node', defaultvalue: "node", description: 'imagem node')
    }
}

docker build -t node .
docker run -p 3000:3000 node



