node {
    stage('Prepare') {
        cleanWs()
        sh 'docker pull jumanjiman/ssllabs-scan:latest'
    }     
    
   stage('Build') {
        checkout scm
        sh 'docker run -v ${WORKSPACE}:/tmp jumanjiman/ssllabs-scan -usecache -grade  -quiet --hostfile /tmp/site.txt'
   }
   
   stage('OUTPUT') {
        def ret = sh(script: 'uname', returnStdout: true)
        println ret
   } 
}

