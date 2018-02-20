node {
    docker.args('--read-only --cap-drop all --rm').image('jumanjiman/ssllabs-scan').inside {
        stage("check ww.elastic2ls.com ") {
        "-usecache -grade -quiet https://www.elastic2ls.com"
        }
    }
}
