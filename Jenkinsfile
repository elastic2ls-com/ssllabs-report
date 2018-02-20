node {
    stage('Prepare') {
        cleanWs()
        // Load seccomp configuration for container
        sh 'docker pull jumanjiman/ssllabs-scan:latest'
    }     
    
   stage('Build') {
        //docker.image('jumanjiman/ssllabs-scan') '-usecache -grade --hostcheck www.elastic2ls.com'
         //sh " docker pull jumanjiman/ssllabs-scan; docker run jumanjiman/ssllabs-scan -usecache -grade -quiet --hostcheck www.elastic2ls.com"
         sh 'docker run -v /tmp:/tmp jumanjiman/ssllabs-scan -usecache -grade  -quiet --hostfile /tmp/sites.txt'
   }
      
}

