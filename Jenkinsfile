pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
               sh '''#!/bin/bash

                docker stop $(docker ps -aq)
                docker rm $(docker ps -aq)
                docker rmi $(docker images)
                docker build -t web .
                #docker login -u akshata9597 -p Akshata@9597
                #docker push akshata9597/web

                #sleep 25
                docker run --name web1 -d -p 8089:80 web'''
            }
        }
    }
}
