pipeline
{
 agent any
 stages
 {
     stage('execute script parallely')  //top level stage
     { 
         parallel                       //add all the parallel stages
         {
           stage('run python scrip')
           { steps { sh 'echo python_script_is_running' }} 

           stage ('run shell script')
           { steps { sh 'echo shell_script_is_running' } }
         }
     }

     stage ('publish python and shell script logs to shared location')
     { steps { sh 'echo upload_logs_to_shared_location' } }
 }

}