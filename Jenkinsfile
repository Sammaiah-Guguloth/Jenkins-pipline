pipeline{
    agent any

    tools {
        nodejs 'node-22'
    }

    stages{
        stage('Fetching Code Changes Detected'){
            steps{
                git branch: 'main', url: 'https://github.com/Sammaiah-Guguloth/Jenkins-pipline'
            }
        }

        stage('Install Dependences'){
            steps{
                sh 'npm install'
            }
        }

        stage('Run application'){
    steps{
        sh 'npm run dev'
    }
}

        // stage('Creating the Docker Image'){
            
        //     steps{
        //         script {
        //             def image = docker.build("yashodaadarsh/devopslab05images:${env.BUILD_NUMBER}", ".")
        //             echo "Docker image created: ${image.id}"
        //         }
        //     }
        // }

        // stage('Running the Docker Container'){
        //     steps{
        //         sh """

        //             echo "Stopping and removing old container (if exists)..."
        //             docker rm -f devopslabcontainer || true

        //             docker run -d \
        //             --name devopslabcontainer \
        //             -p 8081:8081 \
        //             yashodaadarsh/devopslab05images:${env.BUILD_NUMBER}
        //         """
        //     }
        // }
    }
}