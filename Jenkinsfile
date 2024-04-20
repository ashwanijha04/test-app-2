pipeline {
    agent any
    
    stages {
        stage('Install Dependencies') {
            steps {
                // Install Node.js and npm
                // sh 'curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -'
                // sh 'sudo apt-get install -y nodejs'
                
                // Install project dependencies
                sh 'npm install'
            }
        }
        
        stage('Build') {
            steps {
                // Build the React application
                sh 'npm run build'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests if any (you can customize this step based on your testing framework)
                sh 'npm test'
            }
        }
        
        stage('Deploy') {
            steps {
                // You can add deployment steps here, such as deploying to a web server or a cloud service.
                // Example: deploying to AWS S3
                // sh 'aws s3 cp ./build s3://your-s3-bucket-name --recursive --acl public-read'
                sh 'echo hello-world'
            }
        }
    }
    
    post {
        always {
            // Clean up workspace
            cleanWs()
        }
    }
}
