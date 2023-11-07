pipeline {
  agent any
  tools { 
        maven 'Maven_3_6_3'  
    }
   stages{
    stage('SonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey={SonarOrgProjectName} -Dsonar.organization={SonarOrgProjectName} -Dsonar.host.url=https://sonarcloud.io -Dsonar.login={SonarCloudToken}'
			}
        } 
  }
}
