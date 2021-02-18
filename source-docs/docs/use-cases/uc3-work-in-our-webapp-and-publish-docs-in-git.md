---
title: UC3 Work in our App and Publish Docs in GIT
weight: 3
layout: docs
---

In this section we will explain the workflow on how you can work in our Webapp and publish docs in Git. 
The workflow is outlined in the following UML diagram:

<!---
@startuml
skinparam sequence {
ArrowColor DodgerBlue
ActorBorderColor DodgerBlue
LifeLineBorderColor blue
LifeLineBackgroundColor DodgerBlue

ParticipantBorderColor DodgerBlue
ParticipantBackgroundColor DodgerBlue
ParticipantFontName Sans
ParticipantFontSize 17
ParticipantFontColor #A9DCDF

ActorBackgroundColor DodgerBlue
ActorFontColor DodgerBlue
ActorFontSize 17
ActorFontName Sans

}
title Work in our App and Publish Docs in Git
autonumber
actor "Git User" as user
database "PuzzlesCloud" as saas
database "Git Project" as repo
group Git User workflow
   user -> saas : register
   user -> saas : import Git project (simple .md)
   saas -> repo : import Git project (simple .md)
   user -> saas : upload corporate DOCX template
   user -> saas : start a new document in our app
   user -> saas : create a Table of Content from Git .md docs
   user -> saas : save and push
  saas -> repo : push DOCX Template
  saas -> repo : push DOCX Table of Content
  saas -> repo : push updated DOCX and PDF
  alt if using PuzzlesCloud for updates (in development)
   alt if updating content
   user -> saas : update documents
   user -> saas : save and push
   saas -> repo : push updated DOCX and PDF
   else if changing DOCX template
   user -> saas : upload your new DOCX template
   user -> saas : save and push
   saas -> repo : push DOCX Template
   saas -> repo : push updated DOCX and PDF
   else if changing Table of Content (add/remove chapters, change order/heading level)
   user -> saas : Update Table of Content
   user -> saas : save and push
   saas -> repo : push DOCX Table of Content
   saas -> repo : push updated DOCX and PDF
   else if sending DOCX for review
   user -> saas : save and review
   saas -> repo : auto-create a new branch and issue a Pull/Merge request
   else if publishing DOCX
   user -> saas : save and publish
   saas -> repo : auto-approve and merge Pull/Merge Request into master
   end
   end
end
@enduml

preview: https://www.planttext.com/
-->

![Work in our Webapp and Publish Docs in Git](/images/work-in-our-app-and-publish-in-git.png "Work in our Webapp and Publish Docs in Git")