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
        // stage('Deploy')
        // {
        //     steps{withMaven(globalMavenSettingsConfig: '', jdk: 'JDK_home', maven: 'Maven_home', mavenSettingsConfig: '', traceability: true) 
        //         {
        //             sh 'scp -o StrictHostKeyChecking=no target/classes/calcalculator.jar ec2-user@52.28.142.160:/usr/share/tomcat/webapps'
        //         }
        //     }
        // }
    }
}