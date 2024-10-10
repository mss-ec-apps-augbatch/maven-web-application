node
{
 def mavenHome = tool name: "maven3.9.9"

 stage('CheckoutCode')
 {
 git credentialsId: '840b77f7-3ef9-4f1c-becf-f71db09df745', url: 'https://github.com/mss-ec-apps-augbatch/maven-web-application.git'
 }
 stage('Build')
 {
 sh "${mavenHome}/bin/mvn clean package"
 }
 /*
 stage('ExecuteSonarQubeReport')
 {
 sh "${mavenHome}/bin/mvn clean sonar:sonar"
 }
 
  stage('UploadArtifactIntoNexus')
 {
 sh "${mavenHome}/bin/mvn clean deploy"
 }
 stage('DeployAppintoTomcat')
{
sshagent(['bd00ef4d-5c57-4a6c-876a-f530e70ff45e']) {
    sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ubuntu@3.111.40.110:/opt/apache-tomcat-9.0.95/webapps"
}
}
 */
}
