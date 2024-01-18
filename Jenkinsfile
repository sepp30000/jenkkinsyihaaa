pipeline {
  agent any
  stages {
    stage('Estado 1') {
      steps {
        sh 'cat /etc/passwd'
        sh 'echo "Funciona"'
      }
    }

    stage('Estado 2 (Copiar)') {
      parallel {
        stage('Estado 2 (Copiar)') {
          steps {
            sh 'echo "Copiando ficheros"'
          }
        }

        stage('Sleep') {
          steps {
            sh 'sleep 15'
          }
        }

      }
    }

    stage('Notificacion') {
      steps {
        sh 'curl -X POST -H "Content-Type: application/json" -d "{\\"chat_id\\": \\"881875692\\", \\"text\\": \\"Falló la tarea $JOB_NAME!!, ejecución $BUILD_NUMBER,  \\", \\"disable_notification\\": false}" https://api.telegram.org/bot6791917046:AAHuW0hZOl5D5raRyx1R11MWY7fIYHi66xQ/sendMessage'
      }
    }

  }
}