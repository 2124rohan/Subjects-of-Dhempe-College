pipeline {
    agent none
      stages {
            stage ('Non-parallel Stage'){
            steps{
                echo 'This stage will be executed first'
            }
        }


        stage('Run Tests'){
            parallel{
                stage('Test On Windows'){
                    agent{
                        label "Windows11_Node" 
                    }
                    steps{
                        echo "Tasks1 on Agent"
                    }
                }
                stage('Tesk On Master'){

                    steps{
                        echo "Tasks1 On Master"
                    }
                }
            }
        }
    }
}      
