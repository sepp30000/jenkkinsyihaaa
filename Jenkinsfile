pipeline {
  agent any
  stages {
    stage('comprobando index.html') {
      steps {
        sh '''#!/bin/bash
        index=/var/www/index.html
	    ws=/var/jenkins_home/workspace/Tarea3
	    if [ -e $index ]; then rm -rf $index; fi'''
      }
    }
    stage('colocando en volumen el archivo') {
      steps {
        sh 'cp /var/jenkins_home/workspace/Tarea3/index.html /var/www/index.html'
      }
    }

  }
}
