pipeline{
  agent any
  tools{
    maven 'Maven'
  }
  stages{
    stage('Checkout'){
      steps{
        git 'https://github.com/Ranjana2225/ranjana-guava.git'
      }
    }
    stage('Build'){
      steps{
        sh 'mvn clean install'
      }
    }
    stage('adding content'){
      steps{
        sh 'echo "copied content" >source.txt'
      }
    }     
    stage('Run'){
       steps{
          sh 'mvn exec:java -Dexec.mainClass="com.example.App"'
       }
    }
    stage('Verify'){
      steps{
        sh 'cat destination.txt'
      }
    }
  }
}
    
