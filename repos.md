**Multi-Step Workflow**  
Build > Test > Artifact upload  
Created maven.yml file   
.github/workflows/maven.yml   

*******************************************************************************************************************************************
<img width="1898" height="977" alt="image" src="https://github.com/user-attachments/assets/a2f48cfd-8055-493b-8e02-5124fcbb627b" />    
<img width="1917" height="935" alt="image" src="https://github.com/user-attachments/assets/4b3e91c3-e3b9-46e3-8411-e91c4a01f36a" />  
*****************************************************************************************************************************************  

**Secrets and Environment Variables**  
Created main.yaml file .github/workflows/main.yml  
Create Ec2 configure as Self-hosted runner  
Github -> Settings → Secrets and variables → Actions  
Click “New repository secret”  
Add secrets like:  
SSH_HOST = IP  
SSH_USER = ubuntu  
SSH_KEY = private key  

<img width="1915" height="922" alt="image" src="https://github.com/user-attachments/assets/a5e64859-4d05-44d6-99e6-5249609fc29a" />    
<img width="1908" height="962" alt="image" src="https://github.com/user-attachments/assets/5539b5c0-3aa5-498b-aa51-3ba8bfdfd89b" />    
*******************************************************************************************************************************************  
**Deployment Using GitHub Actions Deploy application to a VM or cloud instance Use SSH-based deployment Restart service after deployment **  
Created .github/workflows/deploy.yml file to Deploy  
<img width="1378" height="827" alt="image" src="https://github.com/user-attachments/assets/e3973e5b-5f6c-4bb2-a506-cf872a40e0ce" />  
<img width="1918" height="968" alt="image" src="https://github.com/user-attachments/assets/a0359ea3-c17a-4c93-bc11-b5f39cf7fd46" />  
<img width="1918" height="970" alt="image" src="https://github.com/user-attachments/assets/412dfacd-1bf8-4c54-a789-3d86b8f107d2" />


