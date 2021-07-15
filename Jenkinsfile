node('master')

{ 

stage('ContinuousDownload_master')
         {
    git 'https://github.com/mail2spd04/maven.git'
        }

stage('Continuousbuild_master')
         {
   sh label: '', script: 'mvn package'
        }

}
