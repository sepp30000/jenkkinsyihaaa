pipeline {
  agent any
  stages {
    stage('¿index.html?') {
      steps {
        sh '''#!/bin/bash
        index=/var/www/index.html
	    ws=/var/jenkins_home/workspace/pipeline1
	    if [ -e $index ]; then rm -rf $index; fi'''
      }
    }
  }
}
