pipeline {
    agent any

    tools {
        jdk 'JAVA_HOME'
        maven 'M2_HOME'
    }

    stages {
        stage('GIT') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Hadirgh/timesheetproject.git'
            }
        }

        stage('Compile Stage') {
            steps {
                // se déplacer dans le sous-dossier timesheet avant de lancer Maven
                dir('timesheet') {
                    sh 'mvn clean compile'
                }
            }
        }
    }
}
