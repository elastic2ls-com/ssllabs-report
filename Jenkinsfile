node {
   stage('Build') {
        //docker.image('jumanjiman/ssllabs-scan')  
        //    '-usecache -grade --hostcheck www.elastic2ls.com' 
        //}
      sh { docker pull jumanjiman/ssllabs-scan; docker run -it jumanjiman/ssllabs-scan -usecache -grade -quiet --hostcheck www.elastic2ls.com }
      
}

