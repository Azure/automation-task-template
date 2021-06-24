# automation-task-template
Automation Task Templates

To test the Automation Task template from your forked github repository that holds your template, use Fiddler and in the Fiddler Script find the onBeforeRequest() function and add the following code:

if (oSession.url == "raw.githubusercontent.com/azure/automation-task-template/master/templates/manifest.json") {
            oSession.url = "raw.githubusercontent.com/<git-username>/automation-task-template/<new-branch>/templates/manifest.json"; 
        }
        
        if (oSession.url == "raw.githubusercontent.com/azure/automation-task-template/master/templates/<template-name>") {
            oSession.url = "raw.githubusercontent.com/<git-username>/automation-task-template/<new-branch>/templates/<template-name>";
         }
