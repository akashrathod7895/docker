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
                sh "cp /root/.jenkins/workspace/project/index.html /usr/local/apache2/htdocs"
                
            }
            
        }
        
    }
    
}
