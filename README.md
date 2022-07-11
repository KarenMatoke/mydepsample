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
create a change in a new branch
create a pull request
https://github.com/KarenMatoke/mydepsample/pulls
  https://github.com/KarenMatoke/mydepsample/pull/1
    PR Test results:
       https://app.snyk.io/org/karen.matoke.02/pr-checks/4809b794-60a8-44d0-a69d-aa1cdd4cfafd
       https://app.snyk.io/org/karen.matoke.02/pr-checks/4809b794-60a8-44d0-a69d-aa1cdd4cfafd/license
   
>>>>>>>>>>>>>>>>>>>>>>>

<<<<<<<<<<<<<<<<<<<<<<<   
Login -> Account -> Settings -> Webhooks 
https://github.com/KarenMatoke/mydepsample/settings/hooks

Webhooks allow external services to be notified when certain events happen. When the specified events happen, we’ll send a POST request to each of the URLs you provide. Learn more in our Webhooks Guide.
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
>>>>>>>>>>>>>>>>>>>>>>>

<<<<<<<<<<<<<<<<<<<<<<<  
https://docs.snyk.io/integrations/git-repository-scm-integrations/test-your-prs-for-vulnerabilities-before-merging
>>>>>>>>>>>>>>>>>>>>>>>
