node{
 def mvnhome = tool 'maven'
 stage('SCM'){
      git 'https://github.com/chaitanyasai96/transaction-manager.git '
    }
    stage('build'){ 
         sh '${mvnhome}/bin/mvn clean install'
    }
    post{ 
        echo "Build Success. proceeding to deployment"
    }
   
   
}
