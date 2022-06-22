node{

stage("Source Code From Github"){

git credentialsId: 'Git', url: 'https://github.com/irphan95/java-maven-test.git'

}

stage("Build Docker File"){

sh 'docker build -t $JOB_NAME:V1.$BUILD_ID .'

sh 'docker image tag $JOB_NAME:v1.$BUILD_ID irphan95/$JOB_NAME:V1.$BUILD_ID'

sh 'docker image tag $JOB_NAME:v1.$BUILD_ID irphan95/$JOB_NAME:latest'

}

stage("Push Docker Image To DockerHub"){

sh 'docker login -u=irphan964 -p=irphan@12524'
//sh 'docker login -u irphan964 -p ${irphan@12524}'
}
}
