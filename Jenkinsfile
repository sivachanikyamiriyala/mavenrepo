node('master')
{
 stage('continuousdownload')
  { 
   git 'https://github.com/sivachanikyamiriyala/mavenrepo.git'
  }
 stage('continuousbuild')
  {
   sh 'mvn package'
  }
 stage('continuous deployment')
  {
    sh 'scp /home/ubuntu/.jenkins/workspace/multibranch_master/webapp/target/webapp.war ubuntu@172.31.93.58:/var/lib/tomcat8/webapps/master.war'
  }
}
