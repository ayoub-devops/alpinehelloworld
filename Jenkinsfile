peline {
    agent none
    stages {
        stage('deploy with ansible') {
            agent { docker { image 'dirane/docker-ansible:latest' } }
            steps {
                script {
                    sh '''
                        cd ansible
                        ansible-playbook -i prod.yml alpinehelloworld.yml
                      '''
                }
            }
        }
    }
}
