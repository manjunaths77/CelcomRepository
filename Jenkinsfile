pipeline {
    agent {
        node {
            label 'Dev'
            customWorkspace "/home/manjus/thiru/Dev_C"
        }
    }

    environment {
        PATH = "$HOME/apache-ant-1.10.10/bin:$PATH"
    }
    stages {
        stage('Environment') {
            steps {
                    sh "hostname"
            }
        }

        stage('build') {   
            steps {
            //    ws('/home/jenkins/thiru') {
                    // Run Maven on a Unix agent.
                    sh './build.sh'
            //    }
            }
        }
    }
}
