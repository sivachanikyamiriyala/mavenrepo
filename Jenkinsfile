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
  stage('continuousdeploymen')
  {
   sh 'scp /home/ubuntu/.jenkins/workspace/scriptedpipeline/webapp/target/webapp.war ubuntu@172.31.93.58:/var/lib/tomcat8/webapps/qa.war'
  }
  stage('continuoustesting')
  {
   git 'https://github.com/sivachanikyamiriyala/FunctionalTesting.git'
   sh 'java -jar testing.jar'
  }
  stage('continuousdelivery')
  {
   sh 'scp /home/ubuntu/.jenkins/workspace/scriptedpipeline/webapp/target/webapp.war ubuntu@172.31.94.214:/var/lib/tomcat8/webapps/qa.war'
  }
}
