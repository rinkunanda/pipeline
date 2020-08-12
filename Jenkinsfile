pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '''
                   ./jenkins/build/mvn.sh mvn -B -DskipTests clean package
                   ./jenkins/build/build.sh

                   '''
            }
        }
        stage('Test') {
            steps {
                sh ./jenkins/build/test.sh mvn test
            }
        }
        stage('Push') {
            steps {
                sh 'echo push'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo deploy'
            }
        }
    }
}
