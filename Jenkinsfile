pipeline {

    agent  { label 'slave_1' }
    tools{
    	jdk "${jdk_choice}"
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
