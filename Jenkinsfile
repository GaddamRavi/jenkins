pipeline {
    agent any
    environment{
        project = "Expense"
        com = "Backend"
    }
    options {
        disableConcurrentBuilds()
        timeout(time: 20, unit: 'SECONDS')
    }

    stages {
        stage('Build') {
            steps {
               script{
                 sh """
                    echo "Hello, this is build"
                    echo "This is a $project"
                 """
               }
            }
        }
        stage('Test') {
            steps {
                script{
                 sh """
                    echo "Hello, this is test"
                    echo "Testing is going on $com"
                 """
                }
            }
        }
        stage('Deploy') {
            steps {
                script{
                 sh """
                    echo "Hello, this is deploy"
                 """
                }
            }
        }
    }
     post { 
        always { 
            echo 'I will always say Hello again!'
             
        }
        failure { 
            echo 'I will run when pipeline is failed'
        }
        success { 
            echo 'I will run when pipeline is success'
        }
    }
}
