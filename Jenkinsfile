pipeline {
	agent{
		label {
			label 'built-in'
			customWorkspace '/mnt/docker1'
		}
	}
stages {
	stage (‘container’) {
		steps {
			git url: 'https://github.com/sayalip848/docker.git'
			sh "docker stop centos"
			sh "docker system prune -a -f"
			sh "docker build -t mycentos:2.0 ."
			sh "docker run -itdp 80:80 --name centos mycentos:2.0"
			
			}
		}
	}
}

