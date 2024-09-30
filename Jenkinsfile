pipeline
{
    agent any
    stages
    {
        stage('Build')
        {steps{
                withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_home', maven: 'Maven_home', mavenSettingsConfig: '', traceability: true) 
                {
                    sh 'mvn package'
                }
            }
        }
        stage('Deploy')
        {
            steps{withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_home', maven: 'Maven_home', mavenSettingsConfig: '', traceability: true) 
                {
                    sh 'scp -o StrictHostKeyChecking=no webapp/target/webapp.war ec2-user@172.31.27.20:/usr/share/tomcat/webapps'
                }
            }
        }
    }
}