pipeline{

        agent none

        stages {
                stage('build-java'){
			agent{
                		docker {
                        		image 'maven:3-alpine'
                        		args '-v $HOME/.m2:/root/.m2'
                		}
        		}
                        steps {
                                sh 'mvn -v'
                        }
                }
		stage('build-java-script-node-js'){
                        agent{
                                docker {
                                        image 'node:7-alpine'
                                }
                        }
                        steps { 
                                sh 'node --version'
                        }
                }

        }
}
