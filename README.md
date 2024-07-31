# Ready to Run Kexa Action (Open Source)

<div align="center" id="top">
  <a href="https://www.kexa.io/">
    <img src="readme-images/kexa-no-background-color.png" alt="Logo" width="100" height="100">
  </a>
</div>

## 1. Presentation

**🚀 This is a repository ready to use for Kexa Github action.**
This will allow you to scan you cloud environment quickly and schedule scans in Git Action.
<br/><br/>

### This can help you ensure :
- ✅ Security
- ✅ Compliance
- ✅ Costs saving
- ✅ Alerting of errors or issues
- ✅ General optimization


All addons are already configured, you juste need to set up the credentials for the one you need.
If you already set up credentials, go to the next section too see how to run or schedule the scans.
<br/><br/>

### **How can Kexa Action help you ?**

- ✅ Alerting by Github action logs, MS Teams channel, Email, ... (see section here)
- ✅ Easy-to-run & deploy, no costs
- ✅ Able to export results & data to DB or others services
<br/><br/>

<div align="center">
<h2>
You like the idea or are using this project ? ⤵️ <br/> ⭐ Please star us on the core project Kexa : https://github.com/4urcloud/Kexa ⭐
</h2>
<br/><br/>
</div>

## 2. How to run

### 📦 Installation

Simply fork this repository and make it private, or download the content of the repository and make it private

* Warning * Do not forget to use this repository as a "PRIVATE" reposiroty, you don't want to use Kexa as a public
function because it will display some of your resources ID when raising errors for example.


Go into the new repository you just forked or copied.

### 🔧 Setting Up Addons

Go into "*Settings*", then "*Secrets and variables*", "*Actions*"
Then you can click and add your credentials, following the instructions
above for the addon you wish to use.

<div align="center">
    <img src="readme-images/step1.png" alt="Logo" height="auto">
</div>
<div align="center">
    <img src="readme-images/step2.png" alt="Logo" height="auto">
</div>

##### Azure

* tuto here *

##### Amazon Web Services

* tuto here *

##### Google Cloud Platform

* tuto here *

##### Kubernetes

* tuto here *

##### Github

* tuto here *

##### Helm

* tuto here *

##### Office 365

* tuto here *

### ⏰ Running & Scheduling

<div align="center">
    <img src="readme-images/step3.png" alt="Logo" height="auto">
</div>
<div align="center">
    <img src="readme-images/step4.png" alt="Logo" height="auto">
</div>

**Manual trigger**

Every addon has its associated workflow. (example : for Azure there is azure.yml, AWS there is aws.yml)

Tnere is a global workflow to trigger and schedule all addons at once named "kexa.yml"
This one is just a trigger to call all other workflows.

If you want to try a specific addon manually, click on the workflow from the Github 'Action' page, then
on "run workflow", and then click on "run workflow" again from the pop-up window.

/// SCREEN SHOT HERE ///

By triggering the manual option, you can check that your credentials are correct once you've defined them in the Github repository.

**Scheduled trigger**

As mentioned before, the "kexa.yml" workflow can trigger all other workflows at a certain date/time or interval.

It is defined in the "kexa.yml" as a cronjob, to know more about how to use and define cronjob, you can refer to this documentation : https://pubs.opengroup.org/onlinepubs/9699919799/utilities/crontab.html#tag_20_25_07

// SCREEN SHOT HERE //

You can also use services like https://crontab.guru/ or https://crontab-generator.org/ that will help you write the cronjob you need.

### 🎯 Expected Results

### 🛠️ More configuration options

Kexa git action is based on the core project Kexa : https://github.com/4urcloud/Kexa/
This is just a quick launch repository, but below there is some additionals configuration you can set
without having to read the Kexa core documentation.

To have more advanced options and editing tutorial, refer to the core project documentation.

##### Enabling / Disabling rules, Editing & Error levels

##### Specifying alert channels

You can visualize the results of a scan in the Github workflow logs, but Kexa as a lot more to offer, with different notifications channels such as :

- [x] Email
- [x] Microsoft Teams
- [x] SMS
- [x] Webhook
- [] Jira

Naturally, you'll get a structured, easy-to-read set of results, with as much precision as logs, but less text data.

To know more about how to use those channels : 

##### Using multiple subscriptions/projects for a provider

## 3. Going further with Kexa

This repository is a easy to launch demo of the Kexa script running in Github action, to refer to the core project and the full documentation, follow this link : https://github.com/4urcloud/Kexa

## **Kexa Git action is currently available for :**

- ✅ Azure
- ✅ Amazon Web Services
- ✅ Google Cloud Platform
- ✅ Kubernetes
- ✅ Github
- ✅ Helm
- ✅ Office 365
- ☐ Google Workspace (in re-work for git action)
<br/><br/>
<br/><br/>