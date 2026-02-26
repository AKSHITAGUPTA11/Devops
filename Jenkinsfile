pipeline{
    any agent
    stages{
        stage('GIT-PULL'){
            steps{
                git branch: 'main', url: 'https://github.com/AKSHITAGUPTA11/Devops.git' 
            }
        }
           stage('PLAN'){
            steps{
                echo "build success"
            }
        }
           stage('ARPROVE'){
            steps{
                echo "build success"
            }
        }
             stage('APPLY'){
            steps{
                echo "test success"
            }
        }
             stage('DEPLOY'){
            steps{
                echo "deploy success"
            }
        }
    }
}
