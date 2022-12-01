pipeline {
   agent any
   stages {
       stage('git checkout') {
           steps {
              checkout changelog: false, poll: false, scm: [$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '75c244e7-9103-4f2d-9e8c-fd4d63576851', url: 'https://github.com/Ananthaiah967/Spring-boot-latest.git']]]
           }
       }
      stage('Build and Sonar Analysis') {
			steps{
				 
                    sh 'mvn clean package'
                    
               
			}
		}
   }
}
