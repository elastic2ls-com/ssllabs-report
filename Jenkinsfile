node {
    stage('Prepare') {
        cleanWs()
        sh 'docker pull jumanjiman/ssllabs-scan:latest'
    }     
    
   stage('Build') {
        checkout scm
        sh 'docker run -v ${WORKSPACE}:/tmp jumanjiman/ssllabs-scan -usecache -quiet -json-flat --hostfile /tmp/site.txt > ssh_checks.json'
   }
   stage('Archive') {
   // Archive results
   step([$class: 'ArtifactArchiver', artifacts: '**/*.json'])
   }
}

