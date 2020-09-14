peline {
    agent any

    stages{
       stage('Build') {
          steps{
          echo "Building the application using maven and copying to Ansible server"
          build 	'Build_Job_and_copyto_Ansible_Host'
          }
       }

       stage('Create Docker Image'){
          steps{
           echo "Creating Docker image and pushing to Dockerhub"
           build 'Create_docker_image'
           }
       }

       stage('Create and run container'){
          steps{
          echo "Creating docker container on docker host and exposing app on port 8080"
          build 'Create_and_deploy_Docker_Container'
          }
       }

    }


}

