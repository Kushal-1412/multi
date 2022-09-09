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
        sh "yum install httpd -y"
      }
    }
    stage('deploy-index'){
      steps{
        sh "cp -r index.html /var/www/html/"
        sh "chmod -R 777 /var/www/html/index.html"
      }
    }
    stage('Restart Apache'){
      steps{
        sh "service httpd restart"
      }
    }
    
  }
}
