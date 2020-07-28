node{
    def app
    
    stage('Clone'){
        checkout scm
    }
    stage('Build image'){
        stage('Run image'){
            docker.image(gauthier/nginx).withRun('-p 3000:3000') { c->
                sh 'docker ps'
                sh 'curl localhost'
            }
        }
    }
}