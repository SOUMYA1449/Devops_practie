pipeline{
    agent {label "Demo"}
    
    stages{
        stage("code"){
            steps{
                git url:"https://github.com/SOUMYA1449/Devops_practie.git", branch:"main"
            }
        }
        stage("build"){
            steps{
                echo "code build"
                sh "docker build -t devopspractice:latest ."
            }
        }
        stage("Test"){
            steps{
                echo "code Test"
                sh" docker rm -f Devops_practice || true"
            }
        }
        stage("Deploy"){
            steps{
                echo "code Deploy"
                
                sh "docker run -d -p 8080:80 --name Devops_practice devopspractice:latest "
            }
        }
        
    }
}
