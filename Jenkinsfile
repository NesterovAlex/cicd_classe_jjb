pipeline {

    agent any

    options{
        timestamps ()
    }

    stages{

        stage ('Print ENV') {
          steps {
            echo sh(script: 'env|sort', returnStdout: true)
           }
        }

        stage ('Checkout JJB') {
          steps {
            git url: 'https://github.com/NesterovAlex/cicd_classes_jjb.git'
           }
        }

        stage ('Test JJB') {
          steps {
            sh 'jenkins-jobs --conf jenkins_job.ini test -r jobs/ > /dev/null'
          }
        }

        stage ('Update JJB') {
          when{branch 'master'}
          steps {
            sh 'jenkins-jobs --conf ./jenkins_job.ini update -r jobs/ '
          }
        }

    }


}