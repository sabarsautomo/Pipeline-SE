pipeline {
    agent any

    triggers {
        pollSCM('*/5 * * * 1-5')
    }

    options {
        skipDefaultCheckout(true)
        // Keep the 10 most recent builds
        buildDiscarder(logRotator(numToKeepStr: '10'))
        timestamps()
    }

    environment {
      PATH="$PATH"
    }

    stages {

        stage ("Code pull"){
            steps{
                checkout scm
            }
        }

        stage('Build environment') {
            steps {
                echo "Building virtualenv"
                
            }
        }

        stage('Static code metrics') {
            steps {
                echo "Raw metrics"
                echo "Test coverage"
                echo "Style check"
            }
        }



        stage('Unit tests') {
            steps {
                echo  'Proses..melakukan tes'
            }
        }

        stage('Acceptance tests') {
            steps {
                echo  'Tes..diterima'
            }
        }

        stage('Build package') {
            steps {
                echo  'Build..ok'
            }
        }

	}
}
