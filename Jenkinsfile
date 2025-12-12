pipeline {
    agent any

   stages {
        stage('Clone Repo'){
            steps{
                git branch: 'main', url: 'https://github.com/sinhakiara/security_task'
            }
        }

        stage('Scan the repo with Sonar') {
            steps {
                sh '''
                    
		    cd ./security_task/
                    /sonar-scanner-8.0.1.6346-linux-x64/bin/./sonar-scanner \
  -Dsonar.projectKey=pipeline \
  -Dsonar.sources=. \
  -Dsonar.host.url=https://name-sao-comments-advertisement.trycloudflare.com \
  -Dsonar.token=sqp_2860ce45c93de666fdab8763143ce120cd76693e
                '''
            }
        }
        stage('test1') {
            steps {
                sh '''
                    echo "Sonar scan done"
                '''
            }
        }
    }
}
