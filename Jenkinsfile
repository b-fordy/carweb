node('ubuntu-us-app')
{

def app
stage('Cloning Git')
{
    /* Let's make sure we have the repository cloned to our workspace */
    checkout scm
}

def app
stage('Build-and-Tag')
{
    /* This builds the actual image;
        * This is synonomous to docker build on the command line */
    app.docker.build('blakemfordham/car_docker_repo')    
}

def app
stage('Push-to-Dockerhub')
{
    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub_credentials')    
}

def app
stage('Deploy')
{
    sh 'docker-compose down'
    sh 'docker-compose up -d'
}

}