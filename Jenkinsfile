pipeline {
         agent any 
		 parameters {
                  string defaultValue: 'master', description: 'this is branch will be built', name: 'branch_name'
              }
		 stages{ 
		 
		       stage("Checkout the code "){
			   steps{
			 			 
				 git branch: "$branch_name", url: 'https://github.com/cloud-dev-user/javademo.git'
				    }
				}
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
