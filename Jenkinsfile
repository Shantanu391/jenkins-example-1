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
        }
        
    }
            
            post
            {
                always
                {
                    when {
                        branch 'feature-1'
                    }
                    bat 'git config --global user.email "shantanud391@gmail.com"'
                    bat 'git config --global user.name "Shantanu391"'
                    bat 'git checkout develop'
                    bat 'git merge origin/feature-1'
                }
            }
    
}
