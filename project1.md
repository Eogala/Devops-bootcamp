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

Unzip the contents of the website by running sudo unzip <2137_barista_cafe.zip>
so i ran sudo unzip 2137_barista_cafe.zip.

i Updated nginx configuration by running the command sudo nano /etc/nginx/sites-available/default. Then, edit the root directive within your server block to point to the directory where your downloaded website content is store

I Restart Nginx to apply the changes by running: sudo systemctl restart nginx.

I Open a web browser and go to your Public IPv4 address/Elastic IP address to confirm that your website is working as expected.


##Create An A Record
To make your website accessible via your domain name rather than the IP address, you'll need to set up a DNS record. I did this by buying my domain from Namecheap and then moving hosting to AWS Route 53, where I set up an A record.

On the website i click on Domain List

![pic](img/img34.png)

![pic](img/25.png)

![pic](img/img26.png)

![pic](img/img27.png)

![pic](img/img29.png)

![pic](img/img30.png)


Click on create record again, to create the record for your sub domain.

Input the Record name(www➀), paste your IP address➁, and then click on Create records➂.

Open your terminal and run sudo nano /etc/nginx/sites-available/default to edit your settings. Enter your domain and subdomain names, then save the changes.

![pic](img/25.png)

I Restart your nginx server by running the sudo systemctl restart nginx command.

i Used  domain name in a web browser to verify that your website is accessible.



I Install certbot and Request For an SSL/TLS Certificate

![pic](img/img48.png)
![pic](img/img49.png)
![pic](img/img50.png)
