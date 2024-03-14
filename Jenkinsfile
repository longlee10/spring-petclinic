pipeline {
    agent any

    triggers {
        cron('H/10 * * * 4') // Run every 10 minutes on Thursdays
    }

    stages {
        stage('Build') {
            steps {
                // Clone the repository from GitHub
                git 'https://github.com/longlee10/spring-petclinic.git'

                // Build the application
                bat 'mvn clean package'
            }
        }

        // stage('Code Coverage') {
        //     steps {
        //         // Generate code coverage report using Jacoco
        //         bat 'mvn clean test jacoco:report'
        //     }
        // }
    }
}
