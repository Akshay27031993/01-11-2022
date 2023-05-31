pipeline{
    agent any
    stages{
        stage('Checkout on git'){
            agent any
            steps{
                git 'https://github.com/Akshay27031993/devopsstuff09-devopsclasscodes.git'
            }
        }
        stage('Compile'){
            agent any
            steps{
                sh 'mvn compile'
            }
        }
        stage('CodeReview'){
            agent any
            steps{
                sh 'mvn pmd:pmd'
            }
        }
        stage('UnitTest'){
            agent any
            steps{
                sh 'mvn test'
            }
        }
        stage('Package'){
            agent any
            steps{
                sh 'mvn package'
            }
        }
    }
}
