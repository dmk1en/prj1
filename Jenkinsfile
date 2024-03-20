node {
 stage('SCM') {
 git branch: 'main', credentialsId: 'dmk1en-github', url: 'https://github.com/dmk1en/prj1.git'
 }
 stage('SonarQube Analysis') {
 def scannerHome = tool 'SonarQube Scanner';
 withSonarQubeEnv() {
 sh "${scannerHome}/bin/sonar-scanner -Dsonar.java.binaries=. -Dsonar.projectKey=prj1 -
Dsonar.login=sqa_bc7c2a2c4f99296394a9e7853fa31c7a58e6482c"
 }
 }
}
