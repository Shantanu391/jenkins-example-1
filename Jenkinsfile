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
                    bat 'git config --global user.email "shantanud391@gmail.com"'
                    bat 'git config --global user.name "Shantanu391"'
                    bat 'git add .'
                    bat 'git commit -m "update"'
                    bat 'git checkout develop'
                    bat 'git merge origin/feature-1'
                }
            }
        }
    }
}
