node {
 stage('SCM') {
 git branch: 'main', credentialsId: 'dmk1en-github', url: 'https://github.com/dmk1en/prj1.git'
 }
 stage('SonarQube Analysis') {
 def scannerHome = tool 'SonarQube Scanner';
 withSonarQubeEnv() {
 sh "${scannerHome}/bin/sonar-scanner -Dsonar.java.binaries=. -Dsonar.projectKey=prj1 - Dsonar.login=sqa_236db565975b272c9daa152a9023ce537341d9f4"
 }
 }
}
