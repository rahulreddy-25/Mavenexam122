pipleline{
	agent any
	
	task{
	maven:'maven'
	}
	
	stages{
	  stage('Checkout'){
		steps{
			git branch:'master',url:'https://github.com/rahulreddy-25/Mavenexam122.git'
		}
	  }
	
	  stage('Build'){
		steps{
			sh 'mvn clean package'
		}
	  }
	
	  stage('Test'){
		steps{
			sh 'mvn test'
		}
	  }
	
	  stage('Run Application'){
		steps{
			sh'java -jar target/Mavenexam122-1.0-SNAPSHOT.jar
		}
	  }
	}
	
	post{
		success{
			echo'Build success'
		}
		failure{
			echo'Build fail'
		}
	}
}	
	
	
