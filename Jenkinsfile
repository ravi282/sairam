node('master') 
{
    stage('Cont_down') 
    {
       git 'https://github.com/ravi282/rac.git'
    }
    stage('Cont_bui') 
    {
       sh label: '', script: 'mvn package'
    }
    stage('Cont_Deploy')
    {
       sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/multipipe/webapp/target/webapp.war ubuntu@172.31.84.116:/var/lib/tomcat7/webapps/qaenv.war' 
    }
}
