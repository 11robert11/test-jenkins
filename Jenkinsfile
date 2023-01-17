pipeline {
    agent {
        docker {
            image 'maven:3.8.7-eclipse-temurin-11'
            args '-v /root/.m2:/root/.m2  --dns	127.0.0.1 --net=host'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
            stage('Deliver') {
                steps {
                    sh './deliver.sh'
                    }
                }
    }
}
