


## Using Ansible to Install a RHEL 8 VM Running RH Insights

The purpose of this demo is to familiarize the user with the deployment of applications with Ansible. At the end of this demo, the user should be more familiar with Ansible and how to deploy a virtual machine using an Ansible playbook


## The end result of running this demo

After running this demo, the user should have

* Installed Ansible

* Installed RH Virt-manager (a virtual mahcine environment running RHEL 7)

* RHEL 7 VM

## Products/Technology used

### RHEL

Red Hat Enterprise Linux (RHEL) is Red Hat's commercialized Linux distribution.

### Ansible

Ansible is an automation platform that automates cumbersome, repetitive or complex tasks. The purpose of this demo is to automate a RHEL 7 Virtual Machine installation using Ansible.

### Virt-Manager

Virt-manager is a desktop application that manages all of your virtual machines.

Using a virtual machine is ideal for testing out applications as it gives the user an environment that is low risk. If the virtual machine crashes while the user is testing app functionality, another virtual machine can be made with no ill effects on the actual hardware system.

// ### link:https://www.redhat.com/en/technologies/management/smart-management[Smart Management] (Insights)

// Red Hat Smart Management allows the user to securely manage their RHEL environment using Red Hat Satellite and Red Hat Insights. Smart Management spans across environments, can manage at scale, and can protect your environment from security threats. We will be focusing on Red Hat Insights for this demo.

// Insights is applicable for any system in your organization that needs frequent system checks and is included with a RHEL subscription. Insights helps to identify and remediate threats to security, performance, availability, and stability to avoid issues, outages, and unplanned downtime, and to ensure your Red Hat environment is operating optimally. 



## Requirements to run this demo

* An up to date version of RHEL on a laptop or client system

* Sudo access to your system

* Ansible

* RH Virt-manager

## STEPS

1) First, make sure your system is up to date. You can ensure your system is up to date by running the following command in a command prompt

   $ sudo yum update
   
The terminal will display any packages needed to be installed or updated and prompt you to approve the downloads. Follow the on screen prompts.
   
ifdef::env-github[]
++++
<p align="center">
  <img src="https://github.com/redhat-partner-tech/ansible-demos/blob/main/Ansible_Demo/Folder/Images/RHEL8_Update00.png">
</p>
++++
endif::[]

You'll know your system is completely updated when you see the messsage saying

   Complete!

2) Second, make sure Ansible is installed. If you already have Ansible installed, you can skip this step. If you don't have Ansible installed, go to the Ansible Installation Guide linked here link:https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html[(Install ansible)]

Or just run the following command into a command prompt

   $ sudo yum install ansible  
   
3) Make sure virt-manager is installed. If not already installed, run the following command in your terminal

   $ sudo yum install virt-manager
   
  
4) Prepare a KVM Guest Image 

// Download the ISO  link:https://developers.redhat.com/products/rhel/download[here]
Login to access.redhat.com, click "Download" at the top and download RHEL 7.

Instead of downloading the ISO file to do an installation, download the pre-built KVM Guest image. 

ifdef::env-github[]
++++
<p align="center">
  <img src="https://github.com/redhat-partner-tech/ansible-demos/blob/main/Ansible_Demo/Folder/Images/KVM_Guest_Image.png">
</p>
++++
endif::[]

From this point onwards, we will use Ansible playbooks to automate the creation of a VIrtual Machine

// (create a purpose of this demo documentation list)...
// Overview of demo
// * Why this exists (add a big paragraph at the beginning to define the whole purpose)
// * Outcome/end-result of running demo
// * Products/technology used
// * Requirements (list at top)
// * Steps to re-create/build (add numbered list)




// ### 3) Specify environment variables in the playbook 
// ### 4) Create the virtual machine
// ### 5) Install RHEL8 using the ISO
// ### 6) Post-config and install/setup Red Hat Insights to run

