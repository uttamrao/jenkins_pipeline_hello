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
{sh 'mvn compile'

}
}
}}
}
