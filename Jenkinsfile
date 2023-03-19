pipeline{  
    agent any 
    tools {
        maven "maven3.8.6"
    }
    environment{ 
        DOCKERHUB_CREDENTIALS = credentials("DOCKERHUB_CRED") 
    } 
   stages {
       stage ("1. Git Clone") {
           steps {
               git branch: 'main', url: 'https://github.com/iambowcreek/abc_technologies.git'
           }
       }
       stage('2. Compile SRC'){  
           steps{  
               sh "mvn compile"  
           }  
       }
       stage('3. Test SRC'){  
           steps{  
               sh "mvn test"  
           }  
       }  
       stage('4. Build Package'){  
           steps{  
               sh "mvn clean package"  
           }  
       }  
        stage('5. Docker Build Package'){ 
            steps{
                sh "docker build -t iambowcreek/abc_technologies ." 
            } 
        } 
        stage("6. Push To Dockerhub"){ 
            steps{ 
                sh "echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin"
                sh "docker push iambowcreek/abc_technologies:latest" 
            } 
        }
   }
}