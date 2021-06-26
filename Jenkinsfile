pipeline {
    agent any
    
    tools
    {
        maven 'maven_3_5_0'
    }

    stages {
        stage ('Compile Stage') {

            steps {
                    echo 'mvn clean compile'
            }
        }

        stage ('Testing Stage') {

            steps {
                    echo 'mvn test'
            }
        }


        stage ('Deployment Stage') {
            steps {
                    echo 'mvn deploy'
            }
        }
    }
}
