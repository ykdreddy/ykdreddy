pipeline {
	agent any
	 envinornment{
	  master = 'master'
	  dev = 'dev'
	  stage = 'stage'
	  }
	stages{
	   stage ("SCM Clone repo"){
	       steps{
	         sh "git branch: 'main', credentialsId: 'Git_Credentials', url: 'https://github.com/ykdreddy/complete_kubernetes_prj.git'"
	       }
	   }

	   stage "Build"{
	       steps{
	         sh "mvn clean package"
	       }
	   }

	   stage "test"{
	       steps{
	         script {
	           if (env.branchname == masterbranch){
	               deploy the application
	           }else {
	              echo "skip the deployment for other env"
	           }
	         }
	  
	       }
	   }

	   stage "Deploy the repo"{
	       steps{
	       when {
	            expression { env.ENV_TO_SKP != env.Master_branch}
	       }
	       steps {
	       echo "deploy "

	       }
	       }
	   }
	}
}
