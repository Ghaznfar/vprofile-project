pipeline {
    agent any
    tools {
        jdk 'jdk8'
        maven 'MAVEN3'
    }
    environment {
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASSWORD = 'gh123'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUSIP = '172.31.10.154'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages{
        stage('BUILD'){
            steps {
                sh 'mvn -s settings.xml install -DskipTests'
            }
        }
    }
}