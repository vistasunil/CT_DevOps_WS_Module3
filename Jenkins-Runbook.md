<div align="center">
<img src=https://static.wixstatic.com/media/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png/v1/fit/w_2500,h_1330,al_c/1c706c_a5df0ad56f894928bf858a74ba744b32~mv2.png width="400" height="200">
 </div>

# <div align="center"> JENKINS RUNBOOK </p>

# <div align="center"> DevOps Workshop Training </div>

# <div align="right"> $`\textcolor{brown}{\text{Contact us: }}`$  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; </div>

<div align="right"> T O A C C E L E R A T E Y O U R C A R E E R G R O W T H </div>

### <div align="right"> For questions and more details: </div>

<div align="right"> <img src=https://w7.pngwing.com/pngs/759/922/png-transparent-telephone-logo-iphone-telephone-call-smartphone-phone-electronics-text-trademark-thumbnail.png width="20" height="20"> +91 98712 72900 </div>

<div align="right"> <img src=https://pbs.twimg.com/profile_images/1450734615946219520/jmBHQRRa_400x400.jpg width="20" height="20"> https://www.thecloudtrain.com </div>

<div align="right"> <img src=https://icons.iconarchive.com/icons/martz90/circle/512/email-icon.png width="20" height="20"> support@thecloudtrain.com </div>

<div align="right"> <img src=https://png.pngtree.com/png-vector/20221018/ourmid/pngtree-whatsapp-icon-png-image_6315990.png width="20" height="20"> +91 98712 72900 </div>

#
</br>

## $`\textcolor{red}{\text{NOTE: USE UBUNTU 22.04 VIRTUAL MACHINES FOR ALL THE LABS}}`$

## _Find solutions to your assingment below:_

## Exercise 1: Install Jenkins of GCP server and make sure its enabled and running once installed successfully.**

### _Solution:_

1. Create one GCP Ubuntu 22.04 instance and run below commands one by one. Make sure each command executed successfully before running next command:

**Install Java 11:** Run below commands:

```
sudo apt update
sudo apt install openjdk-11-jre
```

**Install Jenkins:** [Refer official documentation](https://www.jenkins.io/doc/book/installing/linux/) for installation steps.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/6b9fa08c-6013-45bf-80d2-bdf472ff5376)

**Note:** In case you face any issue, refer to the tutorial recording

## Exercise 2: Complete below tasks as part of this exercise:**

1. Create one more GCP server and configure it as slave node to Jenkins you installed in exercise 1:

### _Solution:_

### _a) **Configure Jenkins**_

i. Open browser and enter masterIP:8080.

ii. You should land on a page like this:

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/064df423-b3a9-484e-875d-7de8eb78b6f9)

iii. Copy the path mentioned in the page and perform cat operation in master terminal.

`sudo cat <path>`

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/cb50ba01-8dc3-4efb-8ace-f029b42dda76)

This will give us the password which we will use to unlock our Jenkins.

Copy the password from there and paste it on the Jenkins Server page.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/5a77f5cc-18da-479e-875e-eccfb9f158d9)

iv. Now click on continue. Then click on Install Suggested Plugins.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/7be5b3e7-b056-4742-a139-dff641eafd6a)

v. Once done, enter the Admin User details.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/b48467fa-e89d-4a0f-82be-4d616273a5eb)

Then click on Save and Continue.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/f2e30573-2bff-4094-b437-8a7e1a9ba91e)

Again, click Save and Finish. Click on Install Suggested Plugins. Once it's done, we will land on a page as shown below.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/8c4df3e0-88b7-467c-8298-0ed8e41cd571)

This is our Jenkins Dashboard.

### _b). **Configure Slave nodes**_

i. Go to Manage Jenkins. Click on Configure Global Security.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/8f62fac8-edfc-4451-8bb9-f914f17070c2)

ii. Change the Agents to Random. Then click on Save.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/8f171bbe-0a7c-406b-b1f0-31d657b815c6)

iii. Now go to Manage Nodes.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/cd57e2c4-1899-4606-8dd7-87dc572f2666)

iv. Click on New Node. Add Slave1 as new node and make Permanent Agent. Click on ok.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/d65c5b6c-4f03-4ba7-a0ea-346bc0ac68c3)

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/0e152c88-6ba0-400c-a4a2-cfdf4c024c22)

v. Go to Launch method change it to **Launch agent by connecting it to the controller**.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/93624977-2c41-4135-a099-fa66349861e0)

vi. Then add the current working directory path to **/home/ubuntu/jenkins**. Then click on Save.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/1b785def-56cc-47e7-9813-0c0b5c9fee68)

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/5249709a-526e-4295-bd8f-afc843967d84)

vii. Then click ok. You can see the list of nodes that we have on the Jenkins Dashboard.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/e1b608a2-8539-43ae-bbac-224500e22749)

viii. Go to the Jenkins Dashboard, Click on Slave1. Download the Agent.jar file by clicking on it.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/607ac813-d509-4bf3-abda-e86d2f77de0a)

ix. Now download agent.jar file and upload on the slave ubuntu server using scp, winscp or filezilla.

x. Let us verify if the file has been transferred to Slave1 or not. Open a new session of server. Connect to slave1. Run ls command.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/58847562-96cc-4614-a7c5-96bed3cabb26)

As you can see the agent.jar file appears there, which means our file has been successfully transferred to Slave1.

xi. Before moving ahead install OpenJDK on both Slave1

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/a7535d87-bec8-4424-a4ba-e9f2b47a51f5)

xii. Now install OpenJDK on the server

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/8e1723e7-087b-4598-b488-368490e4e015)

xiii. Connect Slave1 to the Jenkins Server. Go to the Jenkins Dashboard, Click on Slave1, Copy the command line as shown.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/2e835afd-1c86-4c4b-b9a8-0d7752ddc72b)

xiv. Run the command on the slave node as shown below.

_**Note:** If you face any issue with port while connecting agent to master, then open the port show in error on master server by updating the firewall attached to it._

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/afd6f7fd-29c6-4403-897b-aa66d1683e85)

It shows "Connected".

**Important Note:** Don't end the Sessions that we just Connected. To perform further operations on Slave1 duplicate the slave server session.

So now that our Slave1 has been connected to Jenkins Server, it look similar to this.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/9b78058f-d7de-45c2-a502-d91a56104aab)

2. Create a Jenkins job to clone repo _https://github.com/vistasunil/devopsIQ_ and deploy the website inside it the slave instance in container.

### _Solution:_

i. Open your GitHub account and import the below given repository.

_**https://github.com/vistasunil/devopsIQ**_

ii. Install docker on both Slave1

`sudo apt install docker.io`

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/979e72df-344e-4874-bc8c-4cf0c87aa11e)

iii. Open Jenkins Dashboard. Create a new job (Freestyle Project) for Slave1.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/c8cea196-c937-4d9f-9212-d5bea240c196)

iv. Name the Project as Demo, Select Freestyle Project option.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/c99d5df0-3f27-4b3c-a815-e8b08a20ed8f)

Then click on Ok.

You should land on a page like this.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/bfd302d0-f7e9-4c0c-a8c8-b06081512e93)

v. Place your git repository link as shown below.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/9bda1e77-7003-4229-9bcf-8806c275950f)

vi. Click on Restrict where this project can be run. Add Slave1 there.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/4ad9b655-1897-4b3b-a959-7a7deac652ff)

vii. Go to Source Code Management, click on git, add the git repository link there as well.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/7b97c68e-e966-4199-a556-9d1fbfc6061f)

Click on Save.

viii. Click on Build Now, if the building is done without any error there will be blue circle in the building history.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/90a1c885-fa36-4079-ab95-8f3e11c27107)

ix. Click on the blue circle of build #1.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/1bf84792-f1c9-41a6-b94b-1e0badc507a0)

You can see it has been built successfully. Let us verify that.

x. Go to slave1.

```
ls -ltr
cd workspace
ls -ltr
cd Demo
ls -ltr
```

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/98a7b93c-d312-4df7-adf3-e956ddc5d24b)

You can see the repository files there. This means the git repository has been successfully cloned into the Demo job.

**Now we will deploy the website that we have stored in our repository.**

xi. To run the Dockerfile we have to check the copy the present working directory.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/47ef807d-63f6-403a-99ff-f84757c92883)

xii. Now go back to configuring the job. Click on Build, then go to Execute shell

```
sudo docker rm -f $(sudo docker ps -a -q)
sudo docker build /home/ubuntu/jenkins/workspace/Demo -t devopsdemo
sudo docker run -it -p 82:80 -d devopsdemo
```

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/ba5d4c06-8ab0-4224-b304-3c14d69934b9)

Click on save.

xiii. Before building our job again we must add one arbitrary container in slave1. Add container by performing the following command.

`sudo docker run -it -d ubuntu`

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/863cdea9-6202-4390-bcba-95ed1e51c01f)

Now we have added a container as below

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/abb499df-0d3e-4070-a2f6-bff5beabd10a)

xiv. Now open Jenkins Dashboard and build the project.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/f82695cd-bb0e-458e-8210-b235eaaa6e12)

Building was successful.

xv. Now open browser and enter Slave1 Public IP:82. You can get the IP against server name in GCP console

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/8f913b5a-8c76-4537-b985-12ce8f56befb)

This is the apache page that means our container is working perfectly.

xvi. Now enter slave1 _http://<Public IP:82>/devopsIQ/_ in the browser.

![image](https://github.com/vistasunil/CT_DevOps_WS_Module3/assets/37858762/55b74de9-0301-4b42-8930-e4787e9c4a9b)

Website is accessible successfully.

