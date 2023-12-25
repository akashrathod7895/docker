pipeline {
    agent any 
    stages {
        stage ("docker") {
            steps {
                sh "docker run -itdp 80:80 --name container1 httpd bash"
                
            }
            
        }
        stage ("copyfile") {
            steps {
                sh 'docker cp /root/.jenkins/workspace/project/index.html  container1:/usr/local/apache2/htdocs/'
                
            }
            
        }
        stage ("deleteworkspace") {
            steps {
                sh "rm -rf /root/.jenkins/workspace"
            }
        }
        
    }
    
    
}
