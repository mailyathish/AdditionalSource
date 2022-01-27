properties([parameters([string(description: 'Host IP', name: 'HostIP'),string(description: 'ContainerName', name: 'ContainerName')])])
pipeline {
    agent any
    stages {
        stage('Container Stop') {
        steps {
            sshagent(['AWSLogin']) {
                // sh 'docker run -p 9090:9090 -d --name my-app rajuyathi/petclinic-spinnaker-jenkins'
                sh "ssh -o StrictHostKeyChecking=no ubuntu@${params.HostIP} docker rm -f ${params.ContainerName} || true"
            }
             }
            }

            }
            
        
            }
        
    