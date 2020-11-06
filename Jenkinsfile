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
      sh 'py.test --verbose --junit-xml test-reports/results.xml sources/test_calc.py'
      }
     }
     
     stage("deployment")
     {
      steps
      {
      sh 'pyinstaller --onefile sources/add2vals.py'
      }
     }
     
   }

}
