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
                    pip install pysonar || true
		    cd ./security_task/
                    pysonar --sonar-host-url=https://name-sao-comments-advertisement.trycloudflare.com --sonar-token=sqp_2860ce45c93de666fdab8763143ce120cd76693e --sonar-project-key=pipeline
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
