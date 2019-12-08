Pipeline{
agent any
stages{
stage('scm checkout')

steps{
git 'https://github.com/uttamrao/maven-project.git'
}
}
}
{
stage('compile code')
{
steps{
withmaven('mvn:localmaven jdk:localjdk')

{
sh 'mvn compile'}}}
}
}
