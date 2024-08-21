pipeline {
    agent any
    tools {
        maven 'MAVEN3'
        jdk 'Oraclejdk8'
    }
    environment {
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASSWORD = 'gh123'
        RELEASE_REPO = 'vprofile-release'
        CENTERAL_REPO = 'vpro-maven-central'
        NEXUSIP = '172.31.10.154'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages{
        stage('BUILD'){
            steps {
                sh 'mvn clean install -DskipTests'
            }
        }
    }
}