pipeline {
         agent any 
		 parameters {
                  string defaultValue: 'master', description: 'this is branch will be built', name: 'branch_name'
              }
		 stages{ 
		 
		         stage("Build package"){
			   steps{
			       sh " mvn package" 
				   }
				}
			   stage ("build notification"){
			   steps{
			        echo " this build is completed " 
					}
			    }	 
		 }
}
