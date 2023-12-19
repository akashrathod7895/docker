pipeline {
    agent any
    
    stages {
        stage ("clone-repo") {
            steps {
                script {
            // Remove existing 'docker' directory if it exists
            deleteDir()

            // Clone the repository into a new 'docker' directory
            git url: 'https://github.com/akashrathod7895/docker.git', branch: '23q1', dir: 'docker'
        }
                
            }
            
            
        }
        stage ("docker") {
            steps {
                script {
            // Run Docker container with a different host port
            sh 'docker run -itdp 8080:80 httpd'
        }
                
            }
            
        }
        
        stage ("copy-file") {
            steps {
               script {
            // Copy files into the container without using interactive mode
            sh 'docker exec 7f97e58cb15c cp /root/.jenkins/workspace/project/index.html  /usr/local/apache2/htdocs'
        }
        
                
            }
            
        }
        
    }
    
}
