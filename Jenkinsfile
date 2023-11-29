
node {

  
   def IMAGE="srv-web-llr"
	
    stage('Clone') {
          checkout scm
    }

    stage('Build') {
          docker.build("$IMAGE",  '.')
    }

    stage('Run image') {
        docker.image('srv-web').withRun('--name srv_web-llr' ) { c ->

        sh 'docker ps | grep srv_web-llr'
	}

    }
}
