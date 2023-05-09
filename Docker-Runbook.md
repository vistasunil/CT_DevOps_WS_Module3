<div align="center">
<img src=https://static.wixstatic.com/media/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png/v1/fit/w_2500,h_1330,al_c/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png width="400" height="200">
 </div>

# <div align="center"> DOCKER RUNBOOK </p>

# <div align="center"> DevOps Instructor-led Training </div>

<br />

<br />

<br />

<br />

# $${\color{brown} &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; Contact us: &emsp;&emsp;&emsp; }$$

<div align="right"> T O A C C E L E R A T E Y O U R C A R E E R G R O W T H </div>

### <div align="right"> For questions and more details: </div>

<div align="right"> <img src=https://w7.pngwing.com/pngs/759/922/png-transparent-telephone-logo-iphone-telephone-call-smartphone-phone-electronics-text-trademark-thumbnail.png width="20" height="20"> +91 98712 72900 </div>

<div align="right"> <img src=https://pbs.twimg.com/profile_images/1450734615946219520/jmBHQRRa_400x400.jpg width="20" height="20"> https://www.thecloudtrain.com </div>

<div align="right"> <img src=https://icons.iconarchive.com/icons/martz90/circle/512/email-icon.png width="20" height="20"> support@thecloudtrain.com </div>

<div align="right"> <img src=https://png.pngtree.com/png-vector/20221018/ourmid/pngtree-whatsapp-icon-png-image_6315990.png width="20" height="20"> +91 98712 72900 </div>

## _Find solutions to your assingment below:_

## Exercise 1: Install Jenkins of GCP server and make sure its enabled and running once installed successfully.**

### _Solution:_

1. Create one GCP Ubuntu 18.04 instance and run below commands one by one. Make sure each command executed successfully before running next command:

[Refer official documentation](https://www.jenkins.io/doc/book/installing/linux/) for installation steps.

![](RackMultipart20230509-1-a7pl94_html_3101c801e737b9de.png)

**Note:** In case you face any issue, refer to the tutorial recording

## Exercise 2: Complete below tasks as part of this exercise:**

1. Create one more GCP server and configure it as slave node to Jenkins you installed in exercise 1:

### _Solution:_

### _a) **Configure Jenkins**_

i. Open browser and enter masterIP:8080.
ii. You should land on a page like this:

![](RackMultipart20230509-1-a7pl94_html_453b454ece8c866e.png)

iii. Copy the path mentioned in the page and perform cat operation in master terminal.

`sudo cat <path>`

![](RackMultipart20230509-1-a7pl94_html_af7dca9fd4c75c3e.png)

This will give us the password which we will use to unlock our Jenkins.

Copy the password from there and paste it on the Jenkins Server page.

![](RackMultipart20230509-1-a7pl94_html_1296d40ee61ca751.png)

iv. Now click on continue. Then click on Install Suggested Plugins.

![](RackMultipart20230509-1-a7pl94_html_4d3329e2b021b01.png)

v. Once done, enter the Admin User details.

![](RackMultipart20230509-1-a7pl94_html_453f3ee2619364e8.png)

Then click on Save and Continue.

![](RackMultipart20230509-1-a7pl94_html_1136cc3304c0c0ec.png)

Again, click Save and Finish. Click on Install Suggested Plugins. Once it's done, we will land on a page as shown below.

![](RackMultipart20230509-1-a7pl94_html_5c118d1b6cf4e867.png)

This is our Jenkins Dashboard.

### _b). **Configure Slave nodes**_

i. Go to Manage Jenkins. Click on Configure Global Security.

![](RackMultipart20230509-1-a7pl94_html_58a50564c47ff38d.png)

ii. Change the Agents to Random. Then click on Save.

![](RackMultipart20230509-1-a7pl94_html_a074f9fc84ee5bde.png)

iii. Now go to Manage Nodes.

![](RackMultipart20230509-1-a7pl94_html_9f03ce8ea336d050.png)

iv. Click on New Node. Add Slave1 as new node and make Permanent Agent. Click on ok. ![](RackMultipart20230509-1-a7pl94_html_a89fc7701744b4f0.png)

![](RackMultipart20230509-1-a7pl94_html_e148087cd89921f4.png)

v. Go to Launch method change it to **Launch agent by connecting it to the controller**.

![](RackMultipart20230509-1-a7pl94_html_982caa3313b56860.png)

vi. Then add the current working directory path to **/home/ubuntu/jenkins**. Then click on Save.

![](RackMultipart20230509-1-a7pl94_html_484808567aece2e2.png)

![](RackMultipart20230509-1-a7pl94_html_7050f124d8438a5a.png)

vii. Then click ok. You can see the list of nodes that we have on the Jenkins Dashboard.

![](RackMultipart20230509-1-a7pl94_html_5415b23fe2cdf3cc.png)

viii. Go to the Jenkins Dashboard, Click on Slave1. Download the Agent.jar file by clicking on it.

![](RackMultipart20230509-1-a7pl94_html_a8b1227c497376db.png)

ix. Now download agent.jar file and upload on the slave ubuntu server using scp, winscp or filezilla.
x. Let us verify if the file has been transferred to Slave1 or not. Open a new session of server. Connect to slave1. Run ls command.

![](RackMultipart20230509-1-a7pl94_html_ad521919482e0242.png)

As you can see the agent.jar file appears there, which means our file has been successfully transferred to Slave1.

xi. Before moving ahead install OpenJDK on both Slave1

![](RackMultipart20230509-1-a7pl94_html_78947d1fdb090ef1.png)

xii. Now install OpenJDK on the server

![](RackMultipart20230509-1-a7pl94_html_39a4c8b5ee661465.png)

xiii. Connect Slave1 to the Jenkins Server. Go to the Jenkins Dashboard, Click on Slave1, Copy the command line as shown.

![](RackMultipart20230509-1-a7pl94_html_9cda83852ac764bd.png)

xiv. Run the command on the slave node as shown below.

_**Note:** If you face any issue with port while connecting agent to master, then open that port on master server by updating the firewall attached to it._

![](RackMultipart20230509-1-a7pl94_html_7df6e0d54872f0ef.png)

It shows "Connected".

**Important Note:** Don't end the Sessions that we just Connected. To perform further operations on Slave1 duplicate the slave server session.

So now that our Slave1 has been connected to Jenkins Server, it look similar to this.

![](RackMultipart20230509-1-a7pl94_html_6e006c45ae29ff1b.png)

2. Create a Jenkins job to clone repo _https://github.com/vistasunil/devopsIQ_ and deploy the website inside it the slave instance in container.

### _Solution:_

i. Open your GitHub account and import the below given repository.

https://github.com/vistasunil/devopsIQ

ii. Install docker on both Slave1

sudo apt install docker.io

![](RackMultipart20230509-1-a7pl94_html_564b46101c4266bc.png)

iii. Open Jenkins Dashboard. Create a new job (Freestyle Project) for Slave1.

![](RackMultipart20230509-1-a7pl94_html_9f39ad61de45b2d8.png)

iv. Name the Project as Demo, Select Freestyle Project option.

![](RackMultipart20230509-1-a7pl94_html_61abcda0c44c904a.png)

Then click on Ok.

You should land on a page like this.

![](RackMultipart20230509-1-a7pl94_html_e7ee56ccee2e0bc6.png)

v. Place your git repository link as shown below.

![](RackMultipart20230509-1-a7pl94_html_9331ca458c705580.png)

vi. Click on Restrict where this project can be run. Add Slave1 there.

![](RackMultipart20230509-1-a7pl94_html_82064c91312472ab.png)

vii. Go to Source Code Management, click on git, add the git repository link there as well.

![](RackMultipart20230509-1-a7pl94_html_d84abf10c37329cd.png)

Click on Save.

viii. Click on Build Now, if the building is done without any error there will be blue circle in the building history.

![](RackMultipart20230509-1-a7pl94_html_6a4761457921a202.png)

ix. Click on the blue circle of build #1.

![](RackMultipart20230509-1-a7pl94_html_16809ebd55738602.png)

You can see it has been built successfully. Let us verify that.

x. Go to slave1.

```
ls -ltr
cd workspace
ls -ltr
cd Demo
ls -ltr
```

![](RackMultipart20230509-1-a7pl94_html_e31803643a9c10a8.png)

You can see the repository files there. This means the git repository has been successfully cloned into the Demo job.

**Now we will deploy the website that we have stored in our repository.**

xi. To run the Dockerfile we have to check the copy the present working directory.

![](RackMultipart20230509-1-a7pl94_html_70d536615adbe144.png)

xii. Now go back to configuring the job. Click on Build, then go to Execute shell

```
sudo docker rm -f $(sudo docker ps -a -q)
sudo docker build /home/ubuntu/jenkins/workspace/Demo -t devopsdemo
sudo docker run -it -p 82:80 -d devopsdemo
```

![](RackMultipart20230509-1-a7pl94_html_3576e01d3c39b26b.png)

Click on save.

xiii. Before building our job again we must add one arbitrary container in slave1. Add container by performing the following command.

`sudo docker run -it -d ubuntu`

![](RackMultipart20230509-1-a7pl94_html_c9254240f80191d5.png)

Now we have added a container as below

![](RackMultipart20230509-1-a7pl94_html_b1ac7579191f7f73.png)

xiv. Now open Jenkins Dashboard and build the project.

![](RackMultipart20230509-1-a7pl94_html_279a97a7a53e8dea.png)

Building was successful.

xv. Now open browser and enter Slave1 Public IP:82. You can get the IP against server name in GCP console

![](RackMultipart20230509-1-a7pl94_html_faa50689f3d32ca6.png)

This is the apache page that means our container is working perfectly.

xvi. Now enter slave1 _http://<Public IP:82>/devopsIQ/_ in the browser.

![](RackMultipart20230509-1-a7pl94_html_ab74fcb28a0ffe9e.png)

Website is accessible successfully.

