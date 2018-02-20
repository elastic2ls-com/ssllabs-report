node {
    stage('Prepare') {
        cleanWs()
        // Load seccomp configuration for container
        sh 'docker pull jumanjiman/ssllabs-scan:latest'
}     
   stage('Generate list')
      "cat > sites.txt <<"EOF"
      https://www.elastic2ls.com
      https://www.fachadmin.de
      https://github.com
      https://www.google.com   
      EOF"   
      
   stage('Build') {
        //docker.image('jumanjiman/ssllabs-scan') '-usecache -grade --hostcheck www.elastic2ls.com'
         //sh " docker pull jumanjiman/ssllabs-scan; docker run jumanjiman/ssllabs-scan -usecache -grade -quiet --hostcheck www.elastic2ls.com"
         sh 'docker run -itv /tmp:/tmp jumanjiman/ssllabs-scan -usecache -grade  -quiet --hostfile /tmp/sites.txt'
   }
      
}

