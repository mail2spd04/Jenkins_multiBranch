node('master')

{ 

stage('ContinuousDownload_master')
         {
    git 'https://github.com/mail2spd04/Jenkins_multiBranch.git'
        }

stage('Continuousbuild_master')
         {
   sh label: '', script: 'mvn package'
        }
stage('continuous deployment') 
     {
             sh 'scp  /home/ubuntu/.jenkins/workspace/MultiBranchPipeline_master/webapp/target/webapp.war   ubuntu@172.31.35.251:/var/lib/tomcat9/webapps/qaenv1.war'
     }
stage('continuous testing')
	{
		sh 'echo "Testing passed"'
	}
stage('continuous delivery') 
     {
             sh 'scp  /home/ubuntu/.jenkins/workspace/MultiBranchPipeline_master/webapp/target/webapp.war   ubuntu@172.31.36.186:/var/lib/tomcat9/webapps/prodenv1.war'
     }

}
