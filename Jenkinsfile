pipeline {
    agent any 
    stages {
        stage ("docker") {
            steps {
                sh "docker run -it -dp 90:80 --name container1 httpd bash"
                
            }
            
        }
        stage ("copyfile") {
            steps {
                sh 'docker cp /root/.jenkins/workspace/project/index.html  container1:/usr/local/apache2/htdocs'
                
            }
            
        }
        stage ("deleteworkspace") {
            steps {
                sh "rm -f /root/.jenkins/workspace/project/index.html"
            }
        }
        
    }
    
    
}
