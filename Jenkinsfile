node('nodejs') {

 stage('Checkout') {

 git branch: 'main',

 url: 'https://github.com/YOUR_GITHUB_USER/do400-pipelines-control'

 }

 stage('Backend Tests') {

 sh 'node ./backend/test.js'

 }

 stage('Frontend Tests') {

 sh 'node ./frontend/test.js'

 }

}

pipeline {

 agent {

 node {

 label 'nodejs'

 }

 }

 stages {

 stage('Backend Tests') {

 steps {

 sh 'node ./backend/test.js'

 }

 }

 stage('Frontend Tests') {

 steps {
sh 'node ./frontend/test.js'

 }

 }

 }

}
