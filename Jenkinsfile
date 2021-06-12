node('master') 
{
    stage('ContinuousDownload') 
    {
        git 'https://github.com/vaishnavi972/maven.git'
    }
    stage('ContinuousBuild') 
    {
      sh 'mvn package'
    }
    stage('ContinuousDeployment')
    {
    sh 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war ubuntu@172.31.72.129:/var/lib/tomcat8/webapps/test.war'
    }
}
