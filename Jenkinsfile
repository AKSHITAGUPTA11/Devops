pipeline{
    any agent
    stages{
        stage("git-pull"){
            steps{
                git branch: 'main', url: 'https://github.com/AKSHITAGUPTA11/Devops.git' 
            }
        }
           stage("build"){
            steps{
                echo "build success"
            }
        }
             stage("test"){
            steps{
                echo "test success"
            }
        }
             stage("deploy"){
            steps{
                echo "deploy success"
            }
        }
    }
}
