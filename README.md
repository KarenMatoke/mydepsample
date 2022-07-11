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
