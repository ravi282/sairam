node('master') 
{
    stage('Cont_download') 
    {
       git 'https://github.com/ravi282/rac.git'
    }
    stage('Cont_build') 
    {
       sh label: '', script: 'mvn package'
    }
    stage('Cont_Deployment')
    {
       sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/multipipe/webapp/target/webapp.war ubuntu@172.31.84.116:/var/lib/tomcat7/webapps/qaenv.war' 
    }
}
