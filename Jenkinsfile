pipeline{
    agent any
//     environment {
//         PATH = "$PATH:/opt/apache-maven-3.8.2/bin"
//     }
    stages{
       stage('GetCode'){
            steps{
                git 'https://github.com/ani-netizen/Clockock.git'
            }
         }        
//        stage('Build'){
//             steps{
//                 sh 'mvn clean package'
//             }
//          }
        stage('SonarQube analysis') {
//    def scannerHome = tool 'SonarScanner 4.0';
        steps{
        withSonarQubeEnv('SonarQube 9.6.1') { 
        // If you have configured more than one global server connection, you can specify its name
//      sh "${scannerHome}/bin/sonar-scanner"
//         sh "mvn sonar:sonar"
    }
        }
        }
       
    }
}
