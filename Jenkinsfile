node {
  stage ('Build') {
   
    git url: 'https://github.com/Jili14mr/tomcatmavenjava.git'
    withMaven {
      sh "mvn clean install"

    }
  }
  
 
}
