def sayhello(String name)
{
print("HEllo "+name)
}
pipeline{
    
    agent{
        label 'node'
    }
    stages{
    stage("code"){
        steps{
        git branch: 'main', url: 'https://github.com/akshayborse007/jenkins-pipe.git'
        
        }
        
    }    
    
    stage("build"){
        steps{
        
        sh 'mvn clean install'
        sayhello "AB"
        
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
