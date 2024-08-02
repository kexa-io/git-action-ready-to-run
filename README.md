<div align="center" id="top">
  
# Ready to Run Kexa Action (Open Source)
*This is a repository ready to use for a quick launch of Kexa Github action*
</div>

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

Free & Quick scan of your cloud environments for different providers & services <br/><br/>
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
You like the idea or are using this project ? <br/> ⭐ Please star us on the core project Kexa : https://github.com/4urcloud/Kexa ⭐
</h2>
</div>

<div align="center">
<h1>👨‍💻</h1>
<h1>─── How to run ───</h1>
</div>
<br/>

## 📦 1. Installation

Simply fork this repository and make it private, or download the content of the repository and make it private
<br/>

❗ Warning : Do not forget to use this repository as a "*private*" repository, you don't want to use Kexa as a public
function because it will display some of your resources ID when raising errors for example.
<br/>

Go into the new repository you just forked or copied.
<br/>
<br/>
<br/>

## 🔧 2. Setting Up Addons


### **Adding credentials for a providers**

Go into "*Settings*", then "*Secrets and variables*", "*Actions*"<br/>
Then you can click and add your credentials, following the instructions
above for the addon you wish to use.<br/>
<br/>
<div align="center">
    <img src="readme-images/step1.png" alt="Logo" height="auto">
</div>
<div align="center">
    <img src="readme-images/step2.png" alt="Logo" height="auto">
</div>

<br/>
<br/>

### **Required credentials per provider**
*click one to expand and see details*
<br/>
<details>
  <summary>Azure</summary>
<br/>
<div align="center">
  <h3>

  **───────── Azure ─────────** 
  </h3>
</div>
<br/>
From your provider, retrieve the following credentials :<br/><br/>

- *AZURECLIENTID*
- *AZURECLIENTSECRET*
- *AZURETENANTID*
- *SUBSCRIPTIONID*

Set each variable in your github repository secret with the prefix "*AZ1_*"
Prefix is defined in "*/config/azure.json*"

So you will have in your github secrets the following variable with the corresponding
credentials as values:

- *AZ1_AZURECLIENTID*
- *AZ1_AZURECLIENTSECRET*
- *AZ1_AZURETENANTID*
- *AZ1_SUBSCRIPTIONID*

**Ready to run for Azure !**
<br/>
<div align="center">
  <h3>

  **─────────────────────────────────** 
  </h3>
</div>
<br/>
</details>

<details>
  <summary>Amazon Web Services</summary>
<br/>
<div align="center">
  <h3>

  **───────── Amazon Web Services ─────────** 
  </h3>
</div>
<br/>
  From your provider, retrieve the following credentials :<br/><br/>

- *AWS_ACCESS_KEY_ID*
- *AWS_SECRET_ACCESS_KEY*

Set each variable in your github repository secret with the prefix "*AWS1_*"
Prefix is defined in "*/config/aws.json*"

So you will have in your github secrets the following variable with the corresponding
credentials as values:

- *AWS1_AWS_ACCESS_KEY_ID*
- *AWS1_AWS_SECRET_ACCESS_KEY*

**Ready to run for Amazon Web Services !**
<br/>
<div align="center">
  <h3>

  **─────────────────────────────────** 
  </h3>
</div>
<br/>
</details>


<details>
  <summary>Google Cloud Platform</summary>
<br/>
<div align="center">
  <h3>

  **───────── Google Cloud Platform ─────────** 
  </h3>
</div>
<br/>
From your provider, retrieve the following credentials :<br/><br/>

- *GOOGLE_PROJECT_ID*
- *GOOGLE_APPLICATION_CREDENTIALS*

Set each variable in your github repository secret with the prefix "*GCP1_*"
Prefix is defined in "*/config/gcp.json*" and in "*/.github/workflows/gcp.yml*"

So you will have in your github secrets the following variable with the corresponding
credentials as values:

- *GCP1_GOOGLE_PROJECT_ID*
- *GCP1_GOOGLE_APPLICATION_CREDENTIALS*

**Ready to run for Google Cloud Platform !**
<br/>
<div align="center">
  <h3>

  **─────────────────────────────────** 
  </h3>
</div>
<br/>
</details>


<details>
  <summary>Kubernetes</summary>
<br/>
<div align="center">
  <h3>

  **───────── Kubernetes ─────────** 
  </h3>
</div>
<br/>
From your provider, retrieve the following credentials :<br/><br/>

- *KUBECONFIG* (content of ".kube/config")

Set each variable in your github repository secret with the prefix "*KUB1_*"
Prefix is defined in "*/config/kube.json*" and in "*/.github/workflows/kube.yml*"

So you will have in your github secrets the following variable with the corresponding
credentials as values:

- *KUB1_KUBECONFIG*

For Kubernetes, you need to pass the content of your ".kube/config" directly in the Github secret value.

**Ready to run for Kubernetes !**
<br/>
<div align="center">
  <h3>

  **─────────────────────────────────** 
  </h3>
</div>
<br/>
</details>

<details>
  <summary>HTTP</summary>
<br/>
<div align="center">
  <h3>

  **───────── HTTP ─────────** 
  </h3>
</div>
<br/>

See specific configuration for HTTP : https://github.com/4urcloud/Kexa/blob/main/documentation/provider/HTTP.md

**Ready to run for HTTP !**
<br/>
<div align="center">
  <h3>

  **─────────────────────────────────** 
  </h3>
</div>
<br/>
</details>


<details>
  <summary>Github</summary>
<br/>
<div align="center">
  <h3>

  **───────── Github ─────────** 
  </h3>
</div>
<br/>
From your provider, retrieve the following credentials :<br/><br/>

- *GITHUBTOKEN*

Set each variable in your github repository secret with the prefix "*GH1_*"
Prefix is defined in "*/config/git.json*".

So you will have in your github secrets the following variable with the corresponding
credentials as values:

- *GH1_GITHUBTOKEN*

Or else, for the Github addon you can just change the secret name by "GITHUBTOKEN"
instead of the prefix and name. It will take the current permissions on reposiroty.

**Ready to run for Github !**
<br/>
<div align="center">
  <h3>

  **─────────────────────────────────** 
  </h3>
</div>
<br/>
</details>


<details>
  <summary>Helm</summary>
<br/>
<div align="center">
  <h3>

  **───────── Helm ─────────** 
  </h3>
</div>
<br/>
From your provider, retrieve the following credentials :<br/><br/>

- *KUBECONFIG* (content of ".kube/config")

Set each variable in your github repository secret with the prefix "*KUB1_*"
Prefix is defined in "*/config/helm.json*" and in "*/.github/workflows/helm.yml*"

So you will have in your github secrets the following variable with the corresponding
credentials as values:

- *KUB1_KUBECONFIG*

For Helm, you need to pass the content of your ".kube/config" directly in the Github secret value.

**Ready to run for Helm !**
<br/>
<div align="center">
  <h3>

  **─────────────────────────────────** 
  </h3>
</div>
<br/>
</details>


<details>
  <summary>Office 365</summary>
<br/>
<div align="center">
  <h3>

  **───────── Office 365 ─────────** 
  </h3>
</div>
<br/>
  
* tuto here *

<br/>
<div align="center">
  <h3>

  **─────────────────────────────────** 
  </h3>
</div>
<br/>
</details>


<br/>
<br/>
<br/>

## ⏰ 3. Running & Scheduling

<br/><br/>

<div align="center">
<h3>

**Option 1 : Manual trigger (for testing or one shot scan)**

</h3>
</div>
<br/>

Every addon has its associated workflow. (example : for Azure there is azure.yml, AWS there is aws.yml)<br/><br/>
Each addon workflow has a manual trigger, if you want to directly schedule the scan with a date/time or interval,
please keep reading to the next section 'Scheduled Trigger'.<br/>
<br/>
For manual trigger, go to "*Actions*" in your repository, and select the workflow from the addon
you wish to trigger :<br/>
<br/>
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

**Option 2 : Scheduled trigger**

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
<br/>

You can also use services like https://crontab.guru/ or https://crontab-generator.org/ that will help you write the cronjob you need.

<br/>
<br/>
<br/>

## 🎯 4. Expected Results

<br/>
By default, the "*log*" option is activated, so you will have your results in your
Github action logs.
<br/>
<br/>
This section will show you a few example of expected results with explanations.
<br/>
If you want to use another notification channel than "*log*", refer to the next section.
<br/>
<br/>

### Github Action Logs

<br/>
Using this github action, you can simply check the logs by going in 'Actions' and clicking on the associated workflow 'Azure Kexa Action'.
<br/>
You will see the list of alerts with the level, resources ID and rule name and description.
<br/><br/>
<div align="center">
    <img src="readme-images/expected_results_1.png" alt="Logo" height="auto">
</div>
<br/>

### Microsoft Teams

<br/>
By setting up 'teams' notifications, you will get a team card in the channel where you set up the webhook.<br/>
To configure this, refer to the next section.
<br/>
This card will resume the scan results, with all rules that raised an error, with associated resources ID and important informations for remediation.
<br/><br/>
<div align="center">
    <img src="readme-images/expect_teams_2-removebg-preview.png" alt="Logo" height="400">
</div>
<br/>

### Kexa SAAS (no public release yet)

<br/>
SaaS has been developed but is not yet available, it will allow you to visualize your results and resources, having an history of your previous scan with statistics,
browse a rules catalog, use the rule editor.
<br/>
If this interest you, please contact us at contact@4urcloud.eu
<br/><br/>
<div align="center">
    <img src="readme-images/expected_saas-removebg-preview.png" alt="Logo" height="auto">
</div>
<br/>
<br/>
<br/>

## 🛠️ 5. More configuration options

<br/>

### Teams notifications

To enable teams notification, open the rule file you want to be notified of.<br/>
For example, in this repository, the Azure addon is using the "/rules/azureSetRules.yaml" file to scan.<br/>
<br/>
Open this file and in the notification section (at the top-level of the file), add "teams" value in the "type" field.
And add your teams channel webhook in the corresponding "to" field
<br/>
To get your teams channel webhook : https://learn.microsoft.com/en-us/microsoftteams/platform/webhooks-and-connectors/how-to/add-incoming-webhook?tabs=newteams%2Cdotnet
<br/>
You can now set this configuration for each level alert in this file, (you can just set it in the global if you just want global notification).
<br/><br/>
<div align="center">
    <img src="readme-images/webhook_rule.png" alt="Logo" height="auto">
</div>
<br/><br/>
That's it you're ready to get notified !
<br/>
<br/>

### More channels

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
