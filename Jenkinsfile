node {
    docker.image('jumanjiman/ssllabs-scan').args('--read-only --cap-drop all --rm') {
        stage("check ww.elastic2ls.com ") {
        "-usecache -grade -quiet www.elastic2ls.com"
        }
    }
}
