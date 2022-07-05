# Workato Recipes

#### create a contact in salesforce<br>
create a new project<br>
create a new recipe<br>
run on a schedule<br>
show optional fields... start after should be blank<br>
create record in salesforce<br>
create a new connection to salesforce<br>
choose contact... specify the values<br>
save and test the recipe<br>
validate this in salesforce<br>

#### new updated opportunity to create a case<br>
create a new project<br>
create a new recipe<br>
trigger from an app<br>
salesforce - new updated record opportunity<br>
create a new connection to salesforce<br>
trigger condition - stage = Closed Won<br>
search contact in salesforce ... hard code the email value<br>
create case... set fields<br>
create a new opportunity in salesforce<br>
save and test the recipe<br>
check cases<br>

#### customize the job report<br>
jobs... add additional fields... repeat jobs to update<br>

#### conditional actions<br>
log in to atlassian<br>
switch to jira software<br>
create a project... kanban... use template... company managed... give it a name... note the key... <br>
create a new project in workato<br>
create a connection in workato... atlassian account settings... security... create and manage api tokens<br>
new recipe... trigger from an app<br>
create a connection to salesforce... new/updated record (case)<br>
action in an app... jira... choose connection... show optional fields<br>
labels = case number<br>
if condition... list size = 0<br>
yes - create task in jira... issue... configure fields<br>
save changes<br>
if condition... list size = 1<br>


