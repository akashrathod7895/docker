pipeline {
    agent any 
    stages {
        stage ("docker") {
            steps {
                sh "docker run -itdp 8001:80 --name arti3 httpd bash"
                
            }
            
        }
        stage ("copyfile") {
            steps {
                sh 'docker exec arti3 cp /root/.jenkins/workspace/project/index.html  /usr/local/apache2/htdocs/'
                
            }
            
        }
        
    }
    
    
}
