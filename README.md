<h1># Deployment of a URL Shortener application</h1>
<p>Deployment 2 demonstrates my ability to create my own Jenkins Server which allows me to build a CI/CD pipeline for the application and Work with AWS Services such as <em>EC2 </em>which is an a virtural machine on the cloud,<em>Identity and Access Management(IAM)</em> which allows us to have access and manage AWS resources permissions and Elastic Beanstalk; a provisioning infrastructure that allows us to scale and deploy our applications.</p>

<h2>## Steps</h2>
1) Github:
<p>Downloaded the files from Kura and uploaded to a new repository which I named Deployment_Two</p>

2)Setting up SSH connection with EC2 and My local computer:
<p>Next, I realized that to be able to send files to the ec2 from my local computer I need to make sure that there is an SSH Connection </p>
<p>- cd into .ssh and locate id_sa.pub : cd .ssh</p>
<p>- cat into id_sa.pub</p>
<p>- Copy the ssh key</p>
<p>Go to EC2 terminal</p>
<p>cd .ssh </p>
<p>ls  to list the contents in .ssh</p>
<p>sudo nano authorized_keys and paste the ssh key</p>
<p>cat authorized_keys to check if key is there</p>
<p>Go back to local terminal</p>
<p>ssh ubuntu@<my_ec2_instance_public_ip>.Once the keys are present,this code establishes an ssh connection</p>
  
3) Install and Configure Jenkins:
<p>We noe need to Install and configure jenkins. Jenkins allows us to ci/cd pipelines that can run various stages such as build, test etc.CI/CD pipelines provide automation which
takes away the need to manually build and test your python applications for example if you are a developer.</p>
<p>- Install Java: sudo apt-get install fontconfig openjdk-17-jre.Java allows the jenkins application to run and display correctly.</p>
<p>- Source Jenkins repository and add repository and key :

 curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
</p>
<p>- Update: sudo apt update. Make sure that the libraries and binaries are up to date so there won't be an issue of using decrepated resources.
</p>
<p>- Install Jenkins: sudo apt install jenkins </p>
<p>- Start and enable jenkins:

 sudo systemctl start jenkins
 
sudo systemctl enable jenkins

</p>
<p>- Access localhost: <ec2_instance_public ip>:8080
</p>
<p>- Get initial admin password:

 sudo cat /var/lib/jenkins/secrets/initialAdminPassword
</p>
<p>- Paste password</p>

4)Create and Setup AWS IAM Role for Elastic Beanstalk and EC2

5)Create and configure new Amazon Elastic Beanstalk application


<h2>## Plan</h2>>

<img width="572" alt="Screenshot 2023-08-26 at 9 51 52 AM" src="https://github.com/NMonKLabs77/Deployment_Two/assets/139259756/a4e02f76-0b5d-4bb8-8a64-560a86b6403c">


