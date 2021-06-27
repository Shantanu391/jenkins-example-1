pipeline {
    agent any

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
            
            post
            {
                always
                {
                    bat 'git checkout develop'
                    bat 'git merge origin/feature-1'
                }
            }
        }
    }
}
