node('master') 
{
    stage('ContinuousDownload') 
    {
       git 'https://github.com/intelliqittrainings/maven.git'
    }
    stage('ContinuousBuild')
    {
        sh label: '', script: 'mvn package'
    }
    stage('Continous deploy')
    {
	sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/multibranch_master/webapp/target/webapp.war ubuntu@172.31.5.129:/var/lib/tomcat8/webapps/testapp.war'
    }
    
}
