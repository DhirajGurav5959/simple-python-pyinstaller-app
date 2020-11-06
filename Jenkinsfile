pipeline
{
   agent any
   
   stages
   { 
     stage("dev")
     {
      steps
      {
      sh 'python -m py_compile sources/add2vals.py sources/calc.py'
      }
     }
     
     stage("test")
     {
      steps
      {
      echo "testing application"
      }
     }
     
     stage("deployment")
     {
      steps
      {
      echo "deploy application"
      }
     }
     
   }

}
