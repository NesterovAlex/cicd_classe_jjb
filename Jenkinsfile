pipeline {

    agent any

    options{
        timestamps ()
    }

    stages{

        stage ("checkout") {
            steps (
                git url: "https://github.com/NesterovAlex/cicd_classes_jjb.git"
            )
        }

        stage ("Test") {
          steps (
                sh 'ls -l'
            )
        }

    }


}