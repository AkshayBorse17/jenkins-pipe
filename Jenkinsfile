// def sayHello(String name)
// {
// print("HEllo "+name)
// }

@Library('pipeline-library-demo')_


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
             withCredentials([string(credentialsId: 'SONAR_TOKEN', variable: 'SONAR_TOKEN')]) {
            mvn verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar -Dsonar.projectKey=abishere1    
            
                }
        
        sayHello "BC"
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
