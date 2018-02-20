node {
    stage('Prepare') {
        cleanWs()
    }
    stage('Build') {
        // Run lighthouse
        //docker.image('jumanjiman/ssllabs-scan').inside("-usecache -grade -quiet https://www.elastic2ls.com") {
        withDockerContainer(args: '-usecache -grade -quiet https://www.elastic2ls.com', image: 'jumanjiman/ssllabs-scan') {
            // some block
        }    
        //}
    }
    //stage('Archive') {
        // Archive results
    //}
}
