pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo "build section"
            }
        }
        stage('Test'){
            steps{
                sh 'PWD'
                echo "test section"
            }
        }
        stage('Deploy'){
            steps{
                when {
                    expression {
                        currentBuild.result == null || currentBuild.result == 'SUCCESS' 
              }
            }
                echo "Deploy section"
            }

        }
    }


}