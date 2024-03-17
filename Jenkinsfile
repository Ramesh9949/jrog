pipeline{
    agent any
    parameters{

        choice(name: 'action', choices: 'create\ndelete', description: 'Choose create/Destroy')
    }
    stages{
               stage ('Pushing Jfrog File'){
         when { expression {  params.action == 'create' } }
         steps{
           script{
                sh 'curl -X PUT -u admin:Bhavya2912@ -T  /var/lib/jenkins/workspace/Java_app_3.0/target/bhavya.jar "http://13.57.5.246:8082/artifactory/example-repo-local/bhavya.jar"'
               }
           }
       }
          
    }
}
