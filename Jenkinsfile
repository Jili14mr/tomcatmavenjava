node {
  stage ('Build') {
   
    git url: 'https://github.com/Jili14mr/tomcatmavenjava.git'
    withMaven {
      sh "mvn clean install"

    }
  }
  
 stage('Stage1') {
      //steps {
        //script {
          def datas = readYaml file: 'release.yml'
          echo "Got version as ${datas.first} "
          echo "Got version as ${datas.appname} "
          sh '''
          cd /var/lib/jenkins/workspace/Buildjob/target
          ls
          //destination_Artifactory=https://artifactory.build.ge.com/artifactory/
         // path=SXZZG/GPWebUtility/Applications/${UAI}/${datas.appname}/
          curl -k  --user ${artifactory_log_User}:${artifactory_log_Password} -X PUT https://artifactory.build.ge.com/artifactory/SXZZG/GPWebUtility/Applications/${datas.appname} -H 'Content-Type: application/data' --upload-file ${datas.artifactname}
   
        '''
      //  }
       
     // }
    }
 
}
