<<<<<<<<<<<<<<<<<<<<<<<<
/Users/kmm/Documents/code/snyk/codinglanguages/javascript

Run: 
git clone https://github.com/snyk-labs/java-goof.git
mkdir mydepsample
cd mydepsample
git init
cp java-goof/todolist-goof/web.xml .
git add .
mkdir todolist-core
cd todolist-core
cp java-goof/todolist-goof/todolist-core/pom.xml .
git add .
cd ..
mkdir todolist-web-common
cd todolist-web-commmon
cp java-goof/todolist-goof/todolist-web-common/pom.xml .
git add .
git commit -m"commit 3 files"

Run:ls -R
Output:
todolist-core		todolist-web-common	web.xml
./todolist-core:
pom.xml
./todolist-web-common:
pom.xml

github: create new public respository (this one!)

Run:
git branch -M main
git remote add origin https://github.com/KarenMatoke/mydepsample.git
git push -u origin main

app.snyk.io, org: karen.matoke.02, GitHub integration, add respository: mydepsample
click on "Creat web hook"
https://app.snyk.io/org/karen.matoke.02/project/5f0b0335-b12b-4e45-8e40-c1969a66de16/settings/integration
Snyk test for pull requests
Snyk test checks GitHub pull requests for vulnerabilities.
Inherit from Integration settings
Custom
 Enabled
   Fail if the repo has any issues
   
>>>>>>>>>>>>>>>>>>>>>>>>>

<<<<<<<<<<<<<<<<<<<<<<<<
create a change in a new branch that is not main, create a pull request
  for example, under todlist-web-common, edit the pom.xml file and update 2.6.5 to 2.7.7 for the version of com.jasterxml.jackson.core (the snyk vuln results show that that version fixes the vuln)

copy/past from the pull request ('Files changes' tab): 
todolist-web-common/pom.xml
Viewed
@@ -21,7 +21,7 @@
        <dependency>
            <groupId>com.fasterxml.jackson.core</groupId>
            <artifactId>jackson-core</artifactId>
            <version>2.6.5</version>
            <version>2.7.7</version>
        </dependency>
        <dependency>
            <groupId>com.fasterxml.jackson.core</groupId>

create a pull request
https://github.com/KarenMatoke/mydepsample/pulls
  https://github.com/KarenMatoke/mydepsample/pull/1
    PR Test results:
       https://app.snyk.io/org/karen.matoke.02/pr-checks/4809b794-60a8-44d0-a69d-aa1cdd4cfafd
       https://app.snyk.io/org/karen.matoke.02/pr-checks/4809b794-60a8-44d0-a69d-aa1cdd4cfafd/license
On each of the above links, can create a web hook at it gets created in the github repo settings webhooks
   
>>>>>>>>>>>>>>>>>>>>>>>

<<<<<<<<<<<<<<<<<<<<<<<   
Login -> Account -> Settings -> Webhooks 
https://github.com/KarenMatoke/mydepsample/settings/hooks

webhooks are per git repository under the repo "settings"
for this mydepsample repository, go to this URL: https://github.com/KarenMatoke/mydepsample/settings

Webhooks allow external services to be notified when certain "events" happen. When the specified events happen, we’ll send a POST request to each of the URLs you provide. Learn more in our Webhooks Guide.
https://api.snyk.io/webhook/github/b5994935-bf92-47d9-bf73-41679caae75f (pull_request and push)

Payload url
https://api.snyk.io/webhook/github/b5994935-bf92-47d9-bf73-41679caae75f
Content type:
application/json
SSL verification: Enable SSL verification
Let me select individual events:
  Pull requests
  Pushes
Active (We will deliver event details when this hook is triggered

Note that the webhook of snyk to slack is done by configuring the slack integration for a particular snyk org via app.snyk.io
see here: https://snyk.slack.com/apps/A0F7XDUAZ-incoming-webhooks?tab=more_info 
there's a blog about it: https://snyk.io/blog/slack-integration/
my current value for karen.matoke.02: https://hooks.slack.com/services/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
>>>>>>>>>>>>>>>>>>>>>>>

<<<<<<<<<<<<<<<<<<<<<<<  
https://docs.snyk.io/integrations/git-repository-scm-integrations/test-your-prs-for-vulnerabilities-before-merging
>>>>>>>>>>>>>>>>>>>>>>>
