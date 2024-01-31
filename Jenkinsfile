node('built-in') {
    stage('ContineousDownload') {
    git 'https://github.com/palemanudeep/maven.git'
}
   stage('ContineousBuild') {
    sh 'mvn package'
}
stage('ContineousDeploy') {
   deploy adapters: [tomcat9(credentialsId: '2002b68f-4f58-451f-9c84-f9e55cfee074', path: '', url: 'http://13.57.15.57:8080')], contextPath: 'testapp', war: '**/*.war'
}
stage('ContineousTesting')
{
    git 'https://github.com/palemanudeep/Tool.git'
    sh 'java -jar /home/ubuntu/.jenkins/workspace/Scriptedpipeline/testing.jar'
}
stage('ContineousTesting')
{
   deploy adapters: [tomcat9(credentialsId: '2002b68f-4f58-451f-9c84-f9e55cfee074', path: '', url: 'http://54.183.238.175:8080')], contextPath: 'prodapp', war: '**/*.war'
}

}
