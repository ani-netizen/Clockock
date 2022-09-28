node{
stage('SCM Checkout')
{
git branch: 'main', url: 'https://github.com/ani-netizen/Clockock.git'
}
stage('SonarQube analysis')
{
def scannerHome = tool 'sonar-qube';
withSonarQubeEnv('SonarQube 9.6.1')
{
// If you have configured more than one global server connection, you can
// specify its name
bat "${scannerHome}/bin/sonar-scanner"
}
}
}
