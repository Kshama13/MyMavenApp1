pipeline{
agent any 
tools{
maven 'Maven'
}
stages{
	stage('Checkout'){
	steps{
	
		git branch:'master',url: 'https://github.com/Kshama13/MyMavenApp1.git'
		}
		}
	stage('Build'){
	steps{
	sh 'mvn clean package'
	}
	}
	stage('test')
	{
	steps
	{
		sh 'mvn test'
	}
	}
	stage('Run Application')
	{
	steps{
		sh 'java -jar target/MyMavenApp1-1.0-SNAPSHOT.jar'
	}
	}
}
post{
success{
echo 'Build and deployment successful'
}
failure{
echo 'Build Failed'
}}}
	
