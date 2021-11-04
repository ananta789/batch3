pipeline {
    agent any

    stages {
        stage('SOURCECODEMANAGEMENT STAGE') {
            steps {
                echo 'HELLO BATCH3 DEVOPS CHAMPS'
                git 'https://github.com/GiulioDecHit/game.git'
            }
        }
        stage('ARTIFAT BUILD STAGE') {
            steps {
                echo 'BUILDING WITH MAVEN TOOL'
                sh 'mvn clean install'
            }
        }
        stage('deploy to tomcat stage') {
            steps {
                echo 'deploy with tomcat TOOL'
                deploy adapters: [tomcat9(credentialsId: 'e0259c9f-d114-48d9-b32d-aefcec81d2a6', path: '', url: 'http://3.144.119.139:8080/')], contextPath: null, war: '**/*.war'
            }
        }
    }
}
