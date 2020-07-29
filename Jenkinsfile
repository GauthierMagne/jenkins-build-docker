node{
    def app
    
    stage('Clone'){
        checkout scm
    }
    stage('Build image'){
        app = docker.build("gauthier/nginx")
    }    
    
    stage('Run image'){
            docker.image(gauthier/nginx).withRun('-p 3000:3000') 
            {
                sh 'docker ps'
            }
    }
}
