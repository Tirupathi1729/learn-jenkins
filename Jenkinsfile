// pipeline {
//     //agent any
//     agent { node { label 'workstation' } }
//     parameters {
//             string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//
//             text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
//
//             booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
//
//             choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
//
//             password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
//         }
//         triggers { pollSCM('*/1 * * * *') }
//     environment{
//         Test_URl = "google.com"
//         SSH = credentials("centos-ssh")
//     }//hii
//     options{
//         ansiColor('xterm')
//         }
//
//     stages {
//         stage('compile') {
// //             input {
// //                         message "Should we continue?"
// //                         ok "Yes, we should."
// //             }
//             when {
//                             branch 'production'
//             }
//             steps {
//                 echo 'Hello World'
//                 //error 'This is an error'
//                 echo Test_URl
//                 echo SSH
//                 sh 'env'
//                 sh 'ansible -i 172.31.33.112, all -e ansible_user=${SSH_USR} -e ansible_password=${SSH_PSW} -m ping'
//             }
//         }
//
//     }
//     post {
//         always{
//             echo 'post'
//             //send email
//             //trigger some other job
//             //update some jira status about the build
//         }
//     }
// }

// pipeline {
//     agent any
//     stages {
//         stage('Non-Parallel Stage') {
//             steps {
//                 echo 'This stage will be executed first.'
//             }
//         }
//         stage('Parallel Stage') {
//
//             failFast true
//             parallel {
//                 stage('Branch A') {
//                     agent {
//                         label "for-branch-a"
//                     }
//                     steps {
//                         echo "On Branch A"
//                     }
//                 }
//                 stage('Branch B') {
//                     agent {
//                         label "for-branch-b"
//                     }
//                     steps {
//                         echo "On Branch B"
//                     }
//                 }
//                 stage('Branch C') {
//                     agent {
//                         label "for-branch-c"
//                     }
//                     stages {
//                         stage('Nested 1') {
//                             steps {
//                                 echo "In stage Nested 1 within Branch C"
//                             }
//                         }
//                         stage('Nested 2') {
//                             steps {
//                                 echo "In stage Nested 2 within Branch C"
//                             }
//                         }
//                     }
//                 }
//             }
//         }
//     }
// }
//def x :Integer = 10
env.y = 20
def samplef(){
    print "XYZ function"
}
node('workstation'){

    //def x :Integer = 10

    stage('Test'){
            //print x
            sh 'echo y - ${y}'
            samplef()
    }
}