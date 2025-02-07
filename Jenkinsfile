pipeline{
    agents any
    stages {
        stage("Clean") {
            steps {
                deleteDir()
            }            
        }
        stage("clone from git") {
            steps {
                sh "git clone https://github.com/jabedhasan21/java-hello-world-with-maven.git"
            }
        }
        stage("build maven app") {
            steps {
                dir("java-hello-world-with-maven") {
                    sh "mvn clean install"
                }
            }
        }
        stage("test mvn app") {
            steps {
                dir("java-hello-world-with-maven") {
                    sh "mvn test"
                }
            }
        }

    }
}