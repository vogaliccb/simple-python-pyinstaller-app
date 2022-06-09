pipeline {
    agent none 
    stages {
        stage('Buildt') { 
            agent any
            steps {
                sh 'pwd' 
            }
        }
    }
    stages {
        stage('Build') { 
            agent {
                docker {
                    image 'python:2-alpine' 
                }
            }
            steps {
                sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
            }
        }
    }
}
