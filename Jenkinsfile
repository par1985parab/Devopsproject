pipeline 
{
    agent any
    tools 
	{
      maven '3.8.5' 
    }
    stages
    {
        stage('Build')
        {
            steps 
            {
                sh 'mvn clean package'
            }
        }   
    }
	post
	{
	
	   always
	   {
	       emailext body: 'summary', subject: 'pipeline', to: 'parab.vasu1992@gmail.com'
	   }
	   
	 }
}
