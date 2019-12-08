pipeline
{
agent any
stages
{
stage('scm checkout')
{
steps
{
git 'https://github.com/uttamrao/maven-project.git'
}
}
stage('compile code')
{
steps
{
withMaven(jdk: 'localjdk', maven: 'localmaven') 
{
sh 'mvn compile'
}
}
}
stage('test code')
{
steps
{
withMaven(jdk: 'localjdk', maven: 'localmaven') 
{
sh 'mvn test'
}
}
}
stage('build code')
{
steps
{
withMaven(jdk: 'localjdk', maven: 'localmaven') 
{
sh 'mvn package'
}
}
}
stage('deploy to tomcat')
{
steps
{
sshagent (credentials: ['deploy-dev']) 
{
sh 'sh 'scp -o StrictHostKeyChecking=no */target/8.war ec2-user@18.189.2.226:/usr/share/tomcat/webapps'
}
}
}
}
}


