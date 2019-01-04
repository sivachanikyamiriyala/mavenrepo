node('master')
 {
  stage('continuous download')
   {
    git 'https://github.com/sivachanikyamiriyala/mavenrepo.git'
   }
  stage('continuous build')
   {
   sh 'mvn package'
   }
 }

