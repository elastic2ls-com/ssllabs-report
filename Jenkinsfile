node {
    stage('Prepare') {
        cleanWs()
        sh 'docker pull jumanjiman/ssllabs-scan:latest'
    }     
    
   stage('Build') {
        checkout scm
        def ssl = sh (script: '''docker run -v ${WORKSPACE}:/tmp jumanjiman/ssllabs-scan -usecache -grade  -quiet --hostfile /tmp/site.txt''', returnStdout: true)
        println ret
   }
}

