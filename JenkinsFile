pipeline {
        agent none        
        tools {
                maven 'my_mvn'
        }
        stages {
            stage ("Compile") {
                    agent {
                            label "Slave1"
                        }
                steps {
                        sh "mvn compile"
                    }
                }        
            stage("unit test") {  
                    agent {
                            label "Slave2"
                        }
                    steps {
                        sh "mvn test"
                    }
            }
        }
}
