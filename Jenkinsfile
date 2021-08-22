pipeline {

    agent any

    options{
        timestamps ()
    }

    stages{

        stage ('Test') {
          steps (
                sh 'make check'
            )
        }

    }


}