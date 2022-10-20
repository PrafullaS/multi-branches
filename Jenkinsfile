pipeline 
{

	agent 
		{
			label('JS-1')
		}
				
			stages
			{
				stage('Install httpd server')
				{
					steps
						{
							sh "yum install httpd -y"
						}					
				}
				
				stage('Start httpd server')
				{
					steps
					{ 
						sh "systemctl start httpd" 
					}
				}
				
				stage('deploy index file')
				{
					steps
						{
							sh "cp -r index.html /var/www/html/"
							sh "chmod -R 777 /var/www/html/index.html"
						}					
				}
			}
}
