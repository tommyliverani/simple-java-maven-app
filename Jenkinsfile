pipeline {

    agent  { label 'slave_1' }
    parameters {
    	choice(name: 'jdk_choise', choices: ['jdk8', 'jdk11'], description:  'select a jdk version')
    }
    tools{
    	jdk "${params.jdk_choise}"
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
