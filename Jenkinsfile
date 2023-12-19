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
                sh "docker run -itdp 90:80 httpd"
                
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
