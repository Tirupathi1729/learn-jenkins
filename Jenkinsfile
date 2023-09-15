pipeline {
    //agent any
    agent { node { label 'workstation' } }
    parameters {
            string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

            text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

            booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

            choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

            password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
        }
        triggers { pollSCM('*/1 * * * *') }
    environment{
        Test_URl = "google.com"
        SSH = credentials("centos-ssh")
    }//hii
    options{
        ansiColor('xterm')
        }

    stages {
        stage('compile') {
            input {
                        message "Should we continue?"
                        ok "Yes, we should."
            }
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
