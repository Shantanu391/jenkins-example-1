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
                    sh 'git checkout develop'
                    sh 'git merge origin/feature-1'
                }
            }
        }
    }
}
