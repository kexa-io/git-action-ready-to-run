# Ready to Run Kexa Action (Open Source)

<div align="center" id="top">
  <a href="https://www.kexa.io/">
    <img src="readme-images/kexa-no-background-color.png" alt="Logo" width="100" height="100">
  </a>
</div>

<div align="center">
<h1>─── Presentation ───</h1>
<br/>
</div>
<br/>

**🚀 This is a repository ready to use for Kexa Github action.**
This will allow you to scan you cloud environment quickly and schedule scans in Git Action.
<br/><br/>

### This can help you ensure :
- ✅ Security
- ✅ Compliance
- ✅ Costs saving
- ✅ Alerting of errors or issues
- ✅ General optimization


All addons are already configured, you juste need to set up the credentials for the one you need.<br/>
If you already set up credentials, go to the next section too see how to run or schedule the scans.<br/>
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
<br/>
</div>

<div align="center">
<h1>─── How to run ───</h1>
</div>
<br/>

## 📦 1. Installation

Simply fork this repository and make it private, or download the content of the repository and make it private
<br/>
* Warning * Do not forget to use this repository as a "*private*" repository, you don't want to use Kexa as a public
function because it will display some of your resources ID when raising errors for example.
<br/>

Go into the new repository you just forked or copied.
<br/>
<br/>

## 🔧 2. Setting Up Addons

Go into "*Settings*", then "*Secrets and variables*", "*Actions*"<br/>
Then you can click and add your credentials, following the instructions
above for the addon you wish to use.<br/>

<div align="center">
    <img src="readme-images/step1.png" alt="Logo" height="auto">
</div>
<div align="center">
    <img src="readme-images/step2.png" alt="Logo" height="auto">
</div>

<br/>
<br/>

<details>
  <summary>Azure</summary>
  
From your provider, retrieve the following credentials :

- AZURECLIENTID
- AZURECLIENTSECRET
- AZURETENANTID
- SUBSCRIPTIONID

Set each variable in your github repository secret with the prefix "AZ1_"
Prefix is defined in "/config/azure.json"

So you will have :

- AZ1_AZURECLIENTID
- AZ1_AZURECLIENTSECRET
- AZ1_AZURETENANTID
- AZ1_SUBSCRIPTIONID

Ready to run for Azure !
</details>

<details>
  <summary>Amazon Web Services</summary>
  From your provider, retrieve the following credentials :

- AWS_ACCESS_KEY_ID
- AWS_SECRET_ACCESS_KEY

Set each variable in your github repository secret with the prefix "AWS1_"
Prefix is defined in "/config/aws.json"

So you will have :

- AWS1_AWS_ACCESS_KEY_ID
- AWS1_AWS_SECRET_ACCESS_KEY

Ready to run for Amazon Web Services !
</details>


<details>
  <summary>Google Cloud Platform</summary>
From your provider, retrieve the following credentials :

- GOOGLE_PROJECT_ID
- GOOGLE_APPLICATION_CREDENTIALS

Set each variable in your github repository secret with the prefix "GCP1_"
Prefix is defined in "/config/gcp.json" and in "/.github/workflows/gcp.yml"

So you will have :

- GCP1_GOOGLE_PROJECT_ID
- GCP1_GOOGLE_APPLICATION_CREDENTIALS

Ready to run for Google Cloud Platform !
</details>


<details>
  <summary>Kubernetes</summary>
From your provider, retrieve the following credentials :

- KUBECONFIG

Set each variable in your github repository secret with the prefix "KUB1_"
Prefix is defined in "/config/kube.json" and in "/.github/workflows/kube.yml"

So you will have :

- KUB1_KUBECONFIG

Ready to run for Kubernetes !
</details>


<details>
  <summary>Github</summary>

* tuto here *
</details>


<details>
  <summary>Helm</summary>
  
* tuto here *
</details>


<details>
  <summary>Office 365</summary>
  
* tuto here *
</details>


<br/>
<br/>

## ⏰ 3. Running & Scheduling

<br/><br/>

<div align="center">
<h3>

**Manual trigger (for testing or one shot scan)**

</h3>
</div>
<br/>

Every addon has its associated workflow. (example : for Azure there is azure.yml, AWS there is aws.yml)<br/><br/>
Each addon workflow has a manual trigger, if you want to directly schedule the scan with a date/time or interval,
please keep reading to the next section 'Scheduled Trigger'.<br/>
<br/>
For manual trigger, go to "*Actions*" in your repository, and select the workflow from the addon
you wish to trigger :<br/>

<div align="center">
    <img src="readme-images/step3.png" alt="Logo" height="auto">
</div>
<br/><br/>
Then you can click on "run workflow", and then click on "run workflow" again from the pop-up window.
<br/><br/>
<div align="center">
    <img src="readme-images/step4.png" alt="Logo" height="auto">
</div>

<br/><br/>
By triggering the manual option, you can check that your credentials are correct once you've defined them in the Github repository.

<br/><br/>
<div align="center">
<h3>

**Scheduled trigger**

</h3>
</div>
<br/>

Tnere is a global workflow to trigger and schedule all addons at once named "kexa.yml"<br/>
This one is just a trigger to call all other workflows.<br/>
<br/>
It is defined in the "kexa.yml" as a cronjob, to know more about how to use and define cronjob, you can refer to this documentation :<br/>  https://pubs.opengroup.org/onlinepubs/9699919799/utilities/crontab.html#tag_20_25_07 <br/>
<br/>
By default, it will trigger every addons every day at 12:00pm.<br/>
To change this, open "/.github/workflows/kexa.yml" and change the cronjob as you wish<br/>
<br/>

<div align="center">
    <img src="readme-images/stepSchedule.png" alt="Logo" height="auto">
</div>

You can also use services like https://crontab.guru/ or https://crontab-generator.org/ that will help you write the cronjob you need.

<br/>

## 🎯 4. Expected Results

<br/>

## 🛠️ 5. More configuration options

Kexa git action is based on the core project Kexa : https://github.com/4urcloud/Kexa/
This is just a quick launch repository, but below there is some additionals configuration you can set
without having to read the Kexa core documentation.

To have more advanced options and editing tutorial, refer to the core project documentation.

<br/>

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

<div align="center">
<h1>─── Going further with Kexa ───</h1>
<br/>
</div>
<br/>

This repository is a easy to launch demo of the Kexa script running in Github action, to refer to the core project and the full documentation, follow this link : https://github.com/4urcloud/Kexa

<div align="center">
<h1>─── Kexa Git action is currently available for ───</h1>
<br/>
</div>
<br/>

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
