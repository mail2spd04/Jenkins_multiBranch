node('master')

{

stage('ContinuousDownload_loans')
         {
    git 'https://github.com/mail2spd04/Jenkins_multiBranch.git'
        }

stage('Continuousbuild_loans')
         {
   sh label: '', script: 'mvn package'
        }



}
