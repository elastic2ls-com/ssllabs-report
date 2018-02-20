node {
    stage('check ww.elastic2ls.com') {
        docker.image('jumanjiman/ssllabs-scan') {
            "-usecache -grade -quiet www.elastic2ls.com" }
    }
}


//node {
//    stage('check ww.elastic2ls.com') {
//       docker.image('jumanjiman/ssllabs-scan').inside('--read-only --cap-drop all --rm') {
//            "-usecache -grade -quiet www.elastic2ls.com" }
//    }
//}

    
//    node {
//    docker.image('jumanjiman/ssllabs-scan').args('--read-only --cap-drop all --rm') {
//        stage("check ww.elastic2ls.com ") {
//        "-usecache -grade -quiet www.elastic2ls.com"
//        }
//    }
//}
