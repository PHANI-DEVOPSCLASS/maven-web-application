node{
    echo "Job Name is: ${env.JOB_NAME}"
    echo "Node name is: ${env.NODE_NAME}"
def mavenHome = tool name:'maven3.8.5'
//Get the code from Github Repo
stage('CheckoutCode'){
git branch: 'development', credentialsId: 'a69ee4e6-e33b-4ccb-910a-f955e7036384', url: 'https://github.com/PHANI-DEVOPSCLASS/maven-web-application.git'
}
//Do the build by using Maven build tool
stage('Build'){
sh "${mavenHome}/bin/mvn clean package"
}
/*   
//Execute the sonarqube report
stage('ExecuteSonarQubeReport'){
sh "${mavenHome}/bin/mvn sonar:sonar"
}
//Upload Artifacts into Artifactory Repo
stage('UploadArtifactsintoNexus'){
sh "${mavenHome}/bin/mvn deploy"
}
//Deploy Application into Tomcat Server
stage('DeployApplicationIntoTomcatServer'){
sshagent(['8bd87b61-ed83-41a3-afc7-6a02cd80e2de']) {
 sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.111.52.207:/opt/apache-tomcat-9.0.62/webapps/"
}    
}
*/
} 
