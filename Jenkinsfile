pipeline {
	agent any
stages {
	stage (‘container’) {
		steps {
			dir ('/mnt/docker1') {
			sh "docker stop centos"
			sh "docker rm centos"
			git url: 'https://github.com/sayalip848/docker.git'
			sh "echo 'Welcome to my Home page' >> index.html"
			sh "docker build -t mycentos:2.0 ."
			sh "docker run –itdp 80:80 --name centos mycentos:2.0"
			
				}
			}
		}
	}
}

