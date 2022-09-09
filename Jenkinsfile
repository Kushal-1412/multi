pipeline{
  agent{
    label{
      label "172.31.42.111"
      customWorkspace "/data/pipeline"
    }
  }
  stages{
    stage('install-apache'){
      steps{
        sh "sudo yum install httpd -y"
      }
    }
    stage('deploy-index'){
      steps{
        sh "sudo cp -r index.html /var/www/html/"
        sh "sudo chmod -R 777 /var/www/html/index.html"
      }
    }
    stage('Restart Apache'){
      steps{
        sh "sudo service httpd restart"
      }
    }
    
  }
}
