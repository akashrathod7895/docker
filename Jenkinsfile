pipeline {
    agent any 
    stages {
        stage ("docker") {
            steps {
                sh "docker run -itdp 90:80 --name arti httpd bash"
                
            }
            
        }
        stage ("copyfile") {
            steps {
                sh 'docker exec akash cp /root/.jenkins/workspace/project/index.html  /usr/local/apache2/htdocs/'
                
            }
            
        }
        
    }
    
    
}
