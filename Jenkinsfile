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
      //  }
       
     // }
    }
 
}
