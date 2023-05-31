pipeline{
	agent any
      stages{
           stage('Checkout'){
	    
               steps{
		 echo 'cloning..'
                 git 'https://github.com/Akshay27031993/01-11-2022.git'
              }
          }
          stage('Compile'){
             
              steps{
                  echo 'compiling..'
                  bat 'mvn compile'
	      }
          }
          stage('CodeReview'){
		  
              steps{
		    
		  echo 'codeReview'
                  bat 'mvn pmd:pmd'
              }
          }
           stage('UnitTest'){
		  
              steps{
	         
                  bat 'mvn test'
              }
               post {
               success {
                   junit 'target/surefire-reports/*.xml'
               }
           }	
          }
          
          stage('Package'){
		  
              steps{
		  
                  bat 'mvn package'
              }
          }
	     
          
      }
}
