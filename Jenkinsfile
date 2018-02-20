node {
    stage('Prepare') {
        cleanWs()
    }
    stage('Build') {
        // Run lighthouse
        docker.image('jumanjiman/ssllabs-scan') "-usecache -grade -quiet https://www.elastic2ls.com"
    }
    //stage('Archive') {
        // Archive results
    //}
}
