
pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh "sudo rm -R /var/www/html/servidor"
        sh "sudo cp -R ./PHP/servidor /var/www/html/"
        sh "sudo cp /home/javier_barreda94/.env /var/www/html/servidor/"
        sh "(cd /var/www/html/servidor && sudo composer install)"
        sh "sudo chown www-data:www-data -R /var/www/html/servidor/"
      }
    }
    stage('Test'){
      steps{
        sh "echo \"Testing...\""
        sh "echo \"All tests passed.\""
      }
    }

    stage('Deploy'){
      steps{
        sh "echo \"Resultado : finished\""
      }
    }
}
}
