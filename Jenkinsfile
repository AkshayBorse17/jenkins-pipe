pipeline{
    
    agent{
        label 'node'
    }
    stages{
    stage("code"){
        steps{
        git branch: 'main', url: 'https://github.com/akshayborse007/maven-nexus-deployment.git'
        
        }
        
    }    
    
    stage("build"){
        steps{
        sayhello "AB"
        sh 'mvn clean install'
        
        }
    
    }
    
      stage("test"){
        steps{
        
        echo "test"
        
        }
      }
      
        stage("deploy"){
        steps{
        
        echo "deploy"
        
        }
        }
}
}
