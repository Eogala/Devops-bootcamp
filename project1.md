# Documentation
## Create a directory and image folder in VScode
Named folder devops bootcamp where a file (project1.md) was created
## git init to turn directory into resipository


synchronisze Vscode with Github by pushing from local device to github

![2] (img/2.png)

![3] (img/3.png)

## Create Ubuntu server clicking on Ec2 from AWS console

![4](img/img4.png)

Lunch instance and create keypair name

![5](img/img5.png)

![6](img/img6.png)

![7](img/img7.png)

![7](img/img8.png)

Enable SSH, HTTP, and HTTPS access, then proceed to click Launch instance

![pic](img/img9.png)

- Click on the **created instance**.

![pic](img/img10.png)

![pic](img/img11.png)

Copy the command provided under SSH client.

![pic](img/img12.png)

**Open a terminal in the directory where your .pem file was downloaded, paste the command and press Enter.**

![pic](img/img14.png)

## Create And Assign an Elastic IP
Return to your AWS console and click on the menu icon to open the dashboard menu.Select Elastic IPs under Network & Security


![pic](img/img15.png)

![pic](img/img16.png)

##Install Nginx and Setup Your Website using the following command

sudo apt update

sudo apt upgrade

sudo apt install nginx

![pic](img/img18.png)

Go back to your EC2 dashboard and copy your Public IPv4 address

![pic](img/img19.png)

Visit your instances Public IPv4 address in a web browser to view the default Nginx startup page.

![pic](img/img20.png)

**How to obtain the website template URL from tooplate.com:**
Visit Tooplate and select the website template you prefer.

![pic](img/img21.png)


Click the Download button/ inspect/ Hover your mouse cursor over Copy① and then click on Copy URL② from the list that appears on the right

![pic](img/img22.png)


Run this command sudo curl -o /var/www/html/2137_barista_cafe.zip https://www.tooplate.com/zip-templates/2137_barista_cafe.zip to download the websites file to your html directory.

![pic](img/img24.png)
gi


