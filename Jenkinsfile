node
{

def mavenHome= tool name: 'maven3.6.2'

stage('CheckoutCode')
{
git branch: 'development', credentialsId: '45083ce0-8f91-4177-b9b9-570e0d26e939', url: 'https://github.com/MithunTechnologiesDevOps/maven-web-application.git'
}

stage('Build')
{
sh "${mavenHome}/bin/mvn clean package"
}

/*
stage('SonarQubeReportExecution')
{
sh "${mavenHome}/bin/mvn sonar:sonar"
}

stage('UploadArtifactsIntoNexus')
{
sh "${mavenHome}/bin/mvn clean deploy"
}

stage('DeployAppIntoTomcat')
{

sshagent(['1da4f5e9-5116-4d8e-8aa7-5e6213816dfa']) 
{
 sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@13.233.229.244:/opt/apache-tomcat-9.0.34/webapps/"
   
}

}

stage('EmailNotification')
{
emailext body: '''Build is over..

Regards,
Mithun Software Solutions,
9980923226.''', subject: 'Build is over..', to: 'devopstrainingblr@gmail.com'

}
*/


}
