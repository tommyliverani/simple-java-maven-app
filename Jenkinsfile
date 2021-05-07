pipeline {
    agent  any
    tools{
    	jdk "${jdk_choice}"
    	maven 'Apache Maven 3.6.3'
    }
    stages {
        stage('Build') {
            steps {
            	echo "Running with ${env.JAVA_HOME}"
                sh 'mvn -B -DskipTests clean package'        
            }
        }
    }
}
