node{
 def mvnhome = tool 'maven'
 stage('SCM'){
      git 'https://github.com/chaitanyasai96/transaction-manager.git '
    }
    stage('build'){ 
         sh '${mvnhome}/bin/mvn clean install'
    }
  
 stage('deploy'){
  deploy adapters: [tomcat9(credentialsId: 'Tomcat', path: '', url: 'http://3.16.27.161:8070/')], contextPath: null, war: '**/*.war'
  
 }
   
   
}
