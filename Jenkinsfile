pipeline{
    agent{
        label'nodejs'
    }
    stages{
        stage('git pull'){
            steps{
                sh '''
                 cd /var/www
                 mkdir node-test
                 cd /var/www/node-test/
                 git pull
                 '''
            }
        }
        stage('build'){
            steps{
                 sh '''
                 cd  /var/www/node-test/
                 sudo npm install
                 '''
            }
        }
        stage('deploy'){
            steps{
                 sh '''
                 cd /var/www/node-test/
                 sudo npm start
                 '''
            }
        }
    }
}