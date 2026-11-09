pipeline{
    agent any
    stages{
        stage("build Image"){
            steps{
                bat 'docker build -t mydockerimg .'
            }
        }
        stage('Run the image '){
            steps{
                bat 'docker run -d -p 5000:5000 mydockerimg'
            }
        }
    }
    post{
        success{
            echo 'Docker image run successfully'
        }
        failure{
            echo 'Docker failed to run'
        }
    }
}
