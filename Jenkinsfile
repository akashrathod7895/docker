pipeline {
    agent any 
    stages {
        stage ("docker") {
            steps {
                sh "docker run -itdp 90:80 --name arti2 httpd bash"
                
            }
            
        }
        stage ("copyfile") {
            steps {
                sh 'docker exec arti2 cp /root/.jenkins/workspace/project/index.html  /usr/local/apache2/htdocs/'
                
            }
            
        }
        
    }
    
    
}
