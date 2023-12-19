pipeline {
    agent any
    
    stages {
        stage ("clone-repo") {
            steps {
                sh "git clone https://github.com/akashrathod7895/docker.git"
                
            }
            
            
        }
        stage ("docker") {
            steps {
                sh "docker run -itdp 80:80 httpd"
                
            }
            
        }
        
        stage ("copy-file") {
            steps {
                sh "docker exec -it 7f97e58cb15c bash"
                sh "cd htdocs"
                sh "cp /root/.jenkins/workspace/project/index.html ."
                
            }
            
        }
        
    }
    
}
