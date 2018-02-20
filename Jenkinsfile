node {
    stage("check ww.elastic2ls.com ") {
        docker.image('jumanjiman/ssllabs-scan').args('--read-only --cap-drop all --rm') {
        "-usecache -grade -quiet www.elastic2ls.com"
        }
}
