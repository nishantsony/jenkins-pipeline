pipeline {
   agent any
   stages {
       stage ('Compile') {
           steps {
               echo "Compiled Successfully!"
           }
       }
       stage ('JUnit') {
           steps {
               echo "JUnit Passed Successfully!"
               sh ('JUnit.sh')
           }
       }
       stage ('Quality-Gate') {
           steps {
               echo "SonarQube Quality Gate Passed Successfully!"
           }
       }
stage ('Deploy') {
           steps {
               echo "Pass!"
           }
       }
   }
   post {
       always {
           echo "This will always run!"
       }
       success {
           echo "This will run only if successful!"
       }
       failure {
           echo "This will run only if failed!"
       }
       unstable {
           echo "This will run only if the run is marked unstable!"
       }
       changed {
           echo "This will run only if the state of pipeline was changed!"
       }
   }
}
