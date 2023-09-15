pipeline {
    //agent any
    agent { node { label 'workstation' } }
    environment{
        Test_URl = "google.com"
        SSH = credentials("centos-ssh")
    }
    options{
        ansicolor('xterm')
        }

    stages {
        stage('compile') {
            steps {
                echo 'Hello World'
                //error 'This is an error'
                echo Test_URl
                echo SSH
                sh 'env'
                sh 'ansible -i 172.31.33.112, all -e ansible_user=${SSH_USR} -e ansible_password=${SSH_PSW} -m ping'
            }
        }

    }
    post {
        always{
            echo 'post'
            //send email
            //trigger some other job
            //update some jira status about the build
        }
    }
}
