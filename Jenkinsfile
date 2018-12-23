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
}
