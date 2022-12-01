node {
  datas = readYaml file: 'release.yml'

  stage ('Build') {
    datas = readYaml file: 'release.yml'
    git url: 'https://github.com/Jili14mr/tomcatmavenjava.git'
    withMaven {
      sh "mvn clean install"
     // echo "Got version as ${datas.first} "
    }
  }
  
 
}
