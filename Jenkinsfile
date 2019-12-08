Pipeline{
any agent {
stages{
stage('scm checkout')

steps{
git 'https://github.com/uttamrao/jenkins_pipeline_hello.git'
}
}
}
{
stage('compile code')
{
steps{
withmaven('mvn:localmaven jdk:LocalJDk')

{
sh 'mvn compile'}}}
}
}
