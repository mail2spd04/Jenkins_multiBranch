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
stage('continuous deployment') 
     {
             sh 'scp  /home/ubuntu/.jenkins/workspace/MultiBranchPipeline_loans/webapp/target/webapp.war   ubuntu@172.31.35.251:/var/lib/tomcat9/webapps/loans.war'
     }


}
